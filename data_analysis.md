# Data table analysis

Data format can be seen in data description.

## Dictionary

### Level dict

    file: "LEVELDICT.json"
    data:
        'levelname': '未知', 'no': '000'
        'levelname': '其它', 'no': '001'
        'levelname': '物理层', 'no': '100'
        'levelname': '平台层', 'no': '101'
        'levelname': '设备层', 'no': '102'
        'levelname': '协议层', 'no': '200'
        'levelname': 'SDH层 ', 'no': '201'
        'levelname': 'ATM层 ', 'no': '202'
        'levelname': 'IP层', 'no': '203'
        'levelname': 'Link16', 'no': '204'
        'levelname': 'Link11', 'no': '205'
        'levelname': '业务层', 'no': '300'
        'levelname': '指控层', 'no': '301'
        'levelname': '邮件层', 'no': '302'
        'levelname': 'FTP层 ', 'no': '303'
        'levelname': 'HTTP层', 'no': '304'

### Protocol dic

    file: "PROTOCOL_DICT.json"
    data:
        'protocol': '未知', 'no': '000'
        'protocol': '其它', 'no': '001'
        'protocol': 'VAST', 'no': '101'
        'protocol': 'SDH ', 'no': '102'
        'protocol': 'Link16', 'no': '103'
        'protocol': 'Link11', 'no': '104'
        'protocol': 'PPP ', 'no': '201'
        'protocol': 'Ethernet', 'no': '202'
        'protocol': 'HDLC', 'no': '203'
        'protocol': 'IP', 'no': '204'
        'protocol': 'OSPF', 'no': '205'
        'protocol': 'EIGRP ', 'no': '206'
        'protocol': 'ISIS', 'no': '207'
        'protocol': 'PNNI', 'no': '208'
        'protocol': 'CLNP', 'no': '209'
        'protocol': 'ICMP', 'no': '210'
        'protocol': 'ARP ', 'no': '211'
        'protocol': 'TCP ', 'no': '212'
        'protocol': 'UDP ', 'no': '213'
        'protocol': 'BGP ', 'no': '214'
        'protocol': 'RIP ', 'no': '215'
        'protocol': 'HTTP', 'no': '301'
        'protocol': 'FTP ', 'no': '302'
        'protocol': 'SMTP', 'no': '303'
        'protocol': 'POP3', 'no': '304'
        'protocol': 'H.323 ', 'no': '305'
        'protocol': 'SIP ', 'no': '306'
        'protocol': 'DNS ', 'no': '307'
        'protocol': 'SNMP', 'no': '308'

## Simple Analysis

### Analysis based on network

Using network number **\"WL_203_0001\"** as a example:

#### network

Introduction of existed Local networks (e.x. LAN), data updated every a few seconds

    file: "NETWORK.json"
    data example:
    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:00', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:05', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:10', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:15', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:20', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:25', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 188

    'networkno': 'WL_203_0001', 'time': '2016-07-15 14:04:30', 'net_level': '203', 'network_service_type': 'IP', 'net_scale': 190

    ...

#### Link

每个network内的通信情况

    file: "LINK_RELATIONSHIP.json"
    data example:
    'no': 'LJGX_203_630', 'time': '2016-07-15 13:53:15', 'netlevel': '203', 'netno': 'WL_203_0001', 'network_node1': 'WNJD_203_22', 'trans_node_golbalid': 'QJJD_203_3999', 'network_node2': 'WNJD_203_4', 'recv_node_globalid': 'QJJD_203_4049', 'srcaddr': '100.1.1.1', 'destaddr': '100.1.0.17'

    'no': 'LJGX_203_631', 'time': '2016-07-15 13:53:15', 'netlevel': '203', 'netno': 'WL_203_0001', 'network_node1': 'WNJD_203_30', 'trans_node_golbalid': 'QJJD_203_4010', 'network_node2': 'WNJD_203_4', 'recv_node_globalid': 'QJJD_203_4049', 'srcaddr': '100.1.0.29', 'destaddr': '100.1.0.17'

    'no': 'LJGX_203_634', 'time': '2016-07-15 13:53:15', 'netlevel': '203', 'netno': 'WL_203_0001', 'network_node1': 'WNJD_203_99', 'trans_node_golbalid': 'QJJD_203_4017', 'network_node2': 'WNJD_203_6', 'recv_node_globalid': 'QJJD_203_4021', 'srcaddr': '100.0.100.3', 'destaddr': '100.2.0.22'

    'no': 'LJGX_203_639', 'time': '2016-07-15 13:53:15', 'netlevel': '203', 'netno': 'WL_203_0001', 'network_node1': 'WNJD_203_8', 'trans_node_golbalid': 'QJJD_203_4019', 'network_node2': 'WNJD_203_7', 'recv_node_globalid': 'QJJD_203_4022', 'srcaddr': '100.2.2.1', 'destaddr': '100.2.0.21'

    ...(161)

#### Bearing

//TODO

    file: "BEARING_RELATIONSHIP.json"
    data example:
    'bearing_relationship_no': 'CZGX_202_203_319', 'net1no': 'WL_202_0001', 'network_node1_no': 'WNJD_202_75', 'upper_node_global_no': 'QJJD_202_31038', 'net2no': 'WL_203_0001', 'network_node2_no': 'WNJD_203_13', 'lower_node_global_no': 'QJJD_203_30882', 'time': '2016-07-15 10:12:49'

    'bearing_relationship_no': 'CZGX_202_203_320', 'net1no': 'WL_202_0001', 'network_node1_no': 'WNJD_202_76', 'upper_node_global_no': 'QJJD_202_31039', 'net2no': 'WL_203_0001', 'network_node2_no': 'WNJD_203_33', 'lower_node_global_no': 'QJJD_203_30976', 'time': '2016-07-15 10:12:49'

    bearing_relationship_no': 'CZGX_202_203_321', 'net1no': 'WL_202_0001', 'network_node1_no': 'WNJD_202_80', 'upper_node_global_no': 'QJJD_202_31043', 'net2no': 'WL_203_0001', 'network_node2_no': 'WNJD_203_20', 'lower_node_global_no': 'QJJD_203_30892', 'time': '2016-07-15 10:12:49

    bearing_relationship_no': 'CZGX_202_203_322', 'net1no': 'WL_202_0001', 'network_node1_no': 'WNJD_202_78', 'upper_node_global_no': 'QJJD_202_31041', 'net2no': 'WL_203_0001', 'network_node2_no': 'WNJD_203_12', 'lower_node_global_no': 'QJJD_203_30954', 'time': '2016-07-15 10:12:49'

    ...(12)

After filtering, we found there are only three modes:

1. 102-102
2. 202-203
3. 102-101

filter code:

```python
import re
elements = []
for i,element in enumerate(bearR["items"]):
    if re.match('CZGX_102_102',element['bearing_relationship_no'], re.I) or re.match('CZGX_202_203',element['bearing_relationship_no'], re.I):
        continue
    else:
        print(element)
```

result:

**'bearing_relationship_no':'CZGX_102_101_10032'.**

### Analysis based on node

Using network node number **\"WNJD_203_30\"** as an example

#### Network node

    file: "NETWORK_NODE.json"
    data example:
    'network_node_serialno': 'JDLS_203_30', 'time': '2016-07-15 13:52:30', 'net_level': '203', 'netno': 'WL_203_0001', 'network_node_no': 'WNJD_203_30', 'addr': '100.1.0.29', 'global_node_no': 'QJJD_203_2836', 'role': 'R', 'grade': '2', 'node_properties': '2', 'ip': '100.1.0.29', 'os_name': 'UNKNOW', 'sw_name': 'UNKNOW'

    'network_node_serialno': 'JDLS_203_30', 'time': '2016-07-15 14:03:50', 'net_level': '203', 'netno': 'WL_203_0001', 'network_node_no': 'WNJD_203_30', 'addr': '100.1.0.29', 'global_node_no': 'QJJD_203_25857', 'role': 'R', 'grade': '2', 'node_properties': '2', 'ip': '100.1.0.29', 'os_name': 'UNKNOW', 'sw_name': 'UNKNOW'

    'network_node_serialno': 'JDLS_203_30', 'time': '2016-07-15 14:03:55', 'net_level': '203', 'netno': 'WL_203_0001', 'network_node_no': 'WNJD_203_30', 'addr': '100.1.0.29', 'global_node_no': 'QJJD_203_26045', 'role': 'R', 'grade': '2', 'node_properties': '2', 'ip': '100.1.0.29', 'os_name': 'UNKNOW', 'sw_name': 'UNKNOW'

    'network_node_serialno': 'JDLS_203_30', 'time': '2016-07-15 13:59:35', 'net_level': '203', 'netno': 'WL_203_0001', 'network_node_no': 'WNJD_203_30', 'addr': '100.1.0.29', 'global_node_no': 'QJJD_203_16850', 'role': 'R', 'grade': '2', 'node_properties': '2', 'ip': '100.1.0.29', 'os_name': 'UNKNOW', 'sw_name': 'UNKNOW'

    ...

#### Global node

当时有多少个node 是活跃的, 同一时刻同一地址的node的global number是一样的，但是一旦时间发生变化global node number就会改变

At time 2016-07-15 13:52:30, the global node number of **\"WNJD_203_30\"** is **\"QJJD_203_2836\"**.

    file: "GLOBAL_NODE.json"
    data example:
    'global_node_no': 'QJJD_203_2836', 'time': '2016-07-15 13:52:30', 'netlevel': '203', 'networknode_serialno_set': 'JDLS_203_30'

At time 2016-07-15 14:03:50, the global node number of **\"WNJD_203_30\"** is **\"QJJD_203_25857\"**.

    data example:
    'global_node_no': 'QJJD_203_25857', 'time': '2016-07-15 14:03:50', 'netlevel': '203', 'networknode_serialno_set': 'JDLS_203_30'

## Detailed analysis

### Event

暂时理解为link和bearing是流量的传输。

> At time: 2016-07-15 14:45:45

 We discover an event

    'eventno': 'SJ_203_123667'
    'event_name': ''
    'event_begintime': '20160715144545000880'
    'event_endtime': '20160715144545000880'
    'netno': 'WL_203_0001'
    'net_level': '203'
    'trans_node_no': 'WNJD_203_83'
    'trans_node_global_no': 'QJJD_203_124156'
    'recv_node_no': 'WNJD_203_82'
    'recv_node_golbal_no': 'QJJD_203_124171'
    'flow': '140'
    'protocol': '213'
At the same time, we can find node: 'WNJD_203_83' active

    'network_node_serialno': 'JDLS_203_83'
    'time': '2016-07-15 14:45:45'
    'net_level': '203'
    'netno': 'WL_203_0001'
    'network_node_no': 'WNJD_203_83'
    'addr': '100.6.1.10'
    'global_node_no': 'QJJD_203_124156'
    'role': 'endpoint'
    'grade': '1'
    'node_properties': '1'
    'ip': '100.6.1.10'
    'os_name': 'Windows XP'
    'sw_name': 'IE 7'

And connection between 'WNJD_203_83' and 'WNJD_203_10' is also active

    'no': 'LJGX_203_650'
    'time': '2016-07-15 14:45:45'
    'netlevel': '203'
    'netno': 'WL_203_0001'
    'network_node1': 'WNJD_203_83'
    'trans_node_golbalid': 'QJJD_203_124156'
    'network_node2': 'WNJD_203_10'
    'recv_node_globalid': 'QJJD_203_124266'
    'srcaddr': '100.6.1.10'
    'destaddr': '100.6.1.1'

存在protocol_dict中未出现的协议：309

### Node

Now we have a network node called 'WNJD_303_19', we want to know weather it is unique for one IP address.

We search for **'network_node1'='WNJD_303_19' in table *link* :** we found the unique ip address: **100.6.1.9**

> One network node number corresponds to one IP address

Then we search for IP address **100.6.1.9** in *link*, there are two different kinds of results:

    'no': 'LJGX_303_393'
    'time': '2016-07-15 14:10:56'
    'netlevel': '303'
    'netno': 'WL_303-1'
    'network_node1': 'WNJD_303_19'
    'trans_node_golbalid': 'QJJD_303_19'
    'network_node2': 'WNJD_303_38'
    'recv_node_globalid': 'QJJD_303_38'
    'protocol': '302'
    'flow': 40
    'node1_port': 21
    'node2_port': 1046
    'srcaddr': '100.6.1.9'
    'destaddr': '100.5.3.4'

    'no': 'LJGX_203_433'
    'time': '2016-07-15 13:50:36'
    'netlevel': '203'
    'netno': 'WL_203_0001'
    'network_node1': 'WNJD_203_96'
    'trans_node_golbalid': 'QJJD_203_373'
    'network_node2': 'WNJD_203_10'
    'recv_node_globalid': 'QJJD_203_385'
    'srcaddr': '100.6.1.9'
    'destaddr': '100.6.1.1'

The first one is in level 303 with corresponding network node **WNJD_303_19**, the second one is in level 203 with corresponding network node **WNJD_203_96**.

> One IP address have only one corresponding network node in one level, but it can appear in both level 2 and level 3(of course).

### Event节点和relationship中节点的部分关系

event中出现的协议有：205，303，213，212，309，302，104，101，103，301.
其中，协议为205和212的event涉及到的两个节点，在link_relationship有的出现，有的不出现。
协议为103和309的event涉及到的两个节点在link_relationship中从未出现.
其他协议节点都有出现.

## Question

1. Physical link? How do we get the event? What kind of event it is?
2. Link 究竟是指连接情况还是指在那个瞬间有流量交互,同理bearing
3. Link 和 event的关系究竟是什么
4. bearing relationship 里面的upper和lower究竟有什么关系？
