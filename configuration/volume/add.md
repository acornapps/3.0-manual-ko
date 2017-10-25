### 2.5.1    볼륨 추가

볼륨을 추가하여 사용할 수 있습니다.

##### a\)    환경설정 -&gt; 서비스 -&gt; 오른쪽 상단 + 모양의 버튼 클릭![](/image.kh/image.kh/볼륨 추가1.png)

##### b\)    클러스터, 이름, 설명, 정책을 차례로 기입합니다.![](/image.kh/image.kh/볼륨추가2.png)

| **정책** | **설명** |
| :--- | :--- |
| Retain | PersistentVolumeClaim\(PVC\)가 삭제되도 PersistentVolume\(PV\)안에 데이터가 남아있으며 데이터 이동 후 PV를 재사용 할 수 있습니다 |
| Recycle | 적절한 volume plugin이 있다면 사용한 PV가 다시 새로운 Claim을받을 수 있도록 만들어 줍니다. |
| Delete | PVC가 삭제되면서 해당 PV도 함께 삭제되고 그안의 데이터도 모두 삭제됩니다. |

##### 

##### c\) 사용하는 스토리지 플러그인에 따라 스토리지 클래스와 파라미터 설정을 해줍니다.

* ##### NFS 스토리지 플러그인 사용 시![](/assets/nfs.png)

| 스토리지 플러그인 | Network File System |
| :--- | :--- |
| 스토리지 클래스 이름 | cocktail-nfs |
| 파라미터 |  path : NFS server 의 공유폴더 경로                                               server : NFS server 의 IP |

* 아마존 스토리지 플러그인 사용 시

| 스토리지 플러그인 | **설명** |
| :--- | :--- |
| AWS EBS | Amazon public cloud의 스토리지 서비스 |

| 스토리지 클래스 이름 & 파라미터 | 설명 |
| :--- | :--- |
|  | 스토리지 클래스 이름 : |

| **스토리지 플러그인** |
| :--- |


|  | **설명** |
| :--- | :--- |
| Network File System | 네트워크 파일 시스템 |
| AWS EBS | Amazon public cloud의 스토리지 서비스 |
| Google Persistent Disk | Google public cloud의 스토리지 서비스 |
| Azure Disk | Microsoft public cloud의 스토리지 서비스 |


