---
description: L’assistance IP étend vos capacités de gestion des interfaces réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gestion des interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121805"
---
# <a name="managing-interfaces"></a>Gestion des interfaces

L’assistance IP étend vos capacités de gestion des interfaces réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.

Utilisez les fonctions décrites dans les paragraphes suivants pour gérer les interfaces sur l’ordinateur local.

La fonction [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) retourne le nombre d’interfaces sur l’ordinateur local.

La fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) retourne une table qui contient les noms et les index correspondants pour les interfaces sur l’ordinateur local. Pour obtenir des exemples de code impliquant des **GetInterfaceInfo** , consultez [gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

La fonction [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) prend un index d’interface et retourne un index d’interface à compatibilité descendante, c’est-à-dire un index qui utilise uniquement les 24 bits inférieurs. Ce type d’index est parfois appelé index d’interface « convivial ».

La fonction [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) retourne une structure [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) qui contient des informations sur une interface particulière sur l’ordinateur local. Cette fonction requiert que l’appelant fournisse l’index de l’interface.

La fonction [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) retourne une table d' [**entrées \_ IFROW MIB**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , une pour chaque interface sur l’ordinateur.

Utilisez la fonction [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) pour modifier la configuration d’une interface particulière.

 

 
