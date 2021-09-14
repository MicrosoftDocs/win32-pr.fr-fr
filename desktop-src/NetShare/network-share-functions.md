---
description: Les fonctions de partage réseau contrôlent les ressources partagées. Une ressource partagée est une ressource locale sur un serveur (par exemple, un répertoire de disque, un périphérique d’impression ou un canal nommé) accessible par les utilisateurs et les applications sur le réseau.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Fonctions de partage réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021014"
---
# <a name="network-share-functions"></a>Fonctions de partage réseau

Les fonctions de partage réseau contrôlent les ressources partagées. Une ressource partagée est une ressource locale sur un serveur (par exemple, un répertoire de disque, un périphérique d’impression ou un canal nommé) accessible par les utilisateurs et les applications sur le réseau.

Les fonctions de partage sont répertoriées ci-dessous.



| Fonction                                   | Description                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | Partage une ressource sur un serveur.                                       |
| [**NetShareCheck**](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | Demande si un serveur partage un appareil.                        |
| [**NetShareDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | Supprime un nom de partage de la liste des ressources partagées d’un serveur.       |
| [**NetShareEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | Récupère des informations de partage sur chaque ressource partagée sur un serveur.  |
| [**NetShareGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | Récupère des informations sur une ressource partagée spécifiée sur un serveur. |
| [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | Définit les paramètres d’une ressource partagée.                                 |



 

La fonction [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) permet à un utilisateur ou une application de partager une ressource d’un type spécifique à l’aide du nom de partage spécifié. La fonction **NetShareAdd** requiert le nom de partage et le nom de l’appareil local pour partager la ressource. Un utilisateur ou une application doit avoir un compte sur le serveur pour accéder à la ressource.

Vous pouvez également spécifier un descripteur de sécurité à associer à un partage. Les descripteurs de sécurité spécifient les utilisateurs autorisés à accéder aux fichiers via le partage, ainsi que le type d’accès. Spécifiez [**un \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) avec le niveau d’informations [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) lors de l’appel de [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) ou [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo). **NetShareSetInfo** prend en charge le niveau d’informations [**share \_ info \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) . Pour plus d’informations sur les descripteurs de sécurité, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

Les fonctions de gestion de réseau utilisent les noms de partage spéciaux suivants pour la communication interprocessus (IPC) et l’administration à distance du serveur :

-   IPC $, réservé à la communication entre processus
-   ADMIN $, réservé à l’administration à distance
-   $, B $, C $ (et d’autres noms de disque local suivis d’un signe dollar), affectés aux périphériques de disque local

Pour répertorier toutes les connexions établies avec une ressource partagée sur un serveur, ou pour répertorier toutes les connexions établies à partir d’un ordinateur particulier, appelez la fonction [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) . Vous pouvez appeler **NetConnectionEnum** sur les niveaux d’information [**Connection \_ info \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) et [**Connection \_ info \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) .

Les fonctions de partage sont disponibles aux niveaux d’informations suivants :

<dl>

[**Informations de partage \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[**Informations de partage \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[**Informations de partage \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[**PARTAGER des \_ informations \_ 501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[**PARTAGER des \_ informations \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[**PARTAGER des \_ informations \_ 1005**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

Les niveaux d’informations suivants sont valides uniquement pour [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):

<dl>

[**PARTAGER des \_ informations \_ 1004**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[**PARTAGER des \_ informations \_ 1006**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[**PARTAGER des \_ informations \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de partage de gestion de réseau. Pour plus d’informations, consultez [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 
