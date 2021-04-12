---
title: Fonctions serveur (gestion de réseau)
description: Les fonctions du serveur de gestion de réseau effectuent des tâches d’administration sur un serveur local ou distant. Les fonctions de serveur sont répertoriées ci-dessous.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032260"
---
# <a name="server-functions-network-management"></a>Fonctions serveur (gestion de réseau)

Les fonctions du serveur de gestion de réseau effectuent des tâches d’administration sur un serveur local ou distant. Les fonctions de serveur sont répertoriées ci-dessous.



| Fonction                                       | Description                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Retourne une liste de lecteurs de disque locaux sur un serveur.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Répertorie tous les serveurs visibles d’un type particulier (ou types) dans le domaine spécifié. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Retourne les informations de configuration relatives à un serveur spécifié.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Définit les paramètres de fonctionnement d’un serveur.                                        |



 

Seul un utilisateur ou une application ayant l’appartenance à un groupe d’administrateurs sur un serveur local ou distant peut effectuer des tâches d’administration sur ce serveur pour contrôler le fonctionnement du serveur, l’accès utilisateur et le partage des ressources. Les paramètres de bas niveau qui affectent le fonctionnement d’un serveur peuvent être examinés et modifiés en appelant les fonctions [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) et [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) . Ces paramètres sont définis dans le fichier de LANMAN.INI du serveur.

La plupart des fonctions du serveur de gestion de réseau s’exécutent uniquement sur un serveur distant. La fonction [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) s’exécute sur une station de travail locale ou sur un serveur distant. Si vous tentez d’exécuter d’autres fonctions serveur sur une station de travail locale, les fonctions retournent l’erreur NERR \_ RemoteOnly.

Des informations spécifiques au serveur sont disponibles aux niveaux suivants :

-   [**\_Informations sur le serveur \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**\_Informations sur le serveur \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**\_Informations sur le serveur \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**\_Informations sur le serveur \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**\_Informations sur le serveur \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**\_Informations sur le serveur \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**\_Informations sur le serveur \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**\_Informations sur le serveur \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**\_Informations sur le serveur \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**\_Informations sur le serveur \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**\_Informations sur le serveur \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**\_Informations sur le serveur \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**\_Informations sur le serveur \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**\_Informations sur le serveur \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**\_Informations sur le serveur \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**\_Informations sur le serveur \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**\_Informations sur le serveur \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**\_Informations sur le serveur \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**\_Informations sur le serveur \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**\_Informations sur le serveur \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**\_Informations sur le serveur \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**\_Informations sur le serveur \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**\_Informations sur le serveur \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**\_Informations sur le serveur \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**\_Informations sur le serveur \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**\_Informations sur le serveur \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**\_Informations sur le serveur \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**\_Informations sur le serveur \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**\_Informations sur le serveur \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**\_Informations sur le serveur \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**\_Informations sur le serveur \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Si vous programmez pour Active Directory, vous pouvez appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions du serveur de gestion de réseau. Pour plus d’informations, consultez [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Pour plus d’informations, consultez [fonctions de transport serveur et station de travail](server-and-workstation-transport-functions.md).

 

 
