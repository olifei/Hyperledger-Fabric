# Membership
#### 本地和信道MSPs
本地MSPs仅仅在每个节点被定义。但是信道MSPs只在信道中定义一次，每一个信道内的节点都在自己本地存储一份信道MSP的副本。  
#### MSP层级
高层级的MSP关心的是网络管理，低层级的MSP关心的是管理员和私有资源的身份。  
* 网络MSP：通过定义组织参与者的MSPs来定义谁是网络的成员。也定义了那些成员被授权处理管理员任务。  
* 信道MSP：信道MSP是与成员MSP分离的。信道提供了组织间相互交流的私有通道。信道MSP定义了谁有权利参与信道政策的制定，比如添加新的组织和配置chaincode。  
* 成员MSP：本地的MSP是定义在每个节点的文件系统内的。与信道MSP一样，成员MSP也为配置chaincode提供权限。  
* orderer MSP：与成员MSP一样。Orderer只被单独的组织拥有，因此只有单独的一个MSP来定义可信任的成员。  
#### MSP结构
* Root CAs (list)
* Intermediate CAs (list)
* Organizational Units (OUs) (list)
* Administrators (list)
* Revoked Certificates
* Node Identity
* Keystore for Private Key
* TLS Root CA
* TLS Intermediate CA
# Peers
区块链是由peer节点组成的，peer是参与形成账本和是能合约的重要元素。
#### 特殊名词
Fabric系统是通过**chaincode**来实现智能合约的
#### 账本和chaincode
每个peer节点都在本地维护了一个账本和chaincode，这样做的原因是确保分布式结构和区块链去中心化的网络性质。  
