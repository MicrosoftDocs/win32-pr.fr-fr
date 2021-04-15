---
title: Fonctions Netfile (gestion de réseau)
description: Les fonctions de fichiers de gestion de réseau permettent de surveiller et de fermer les ressources de fichier, de périphérique et de canal ouvertes sur un serveur. Les fonctions de fichier sont répertoriées ci-dessous.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508261"
---
# <a name="netfile-functions-network-management"></a>Fonctions Netfile (gestion de réseau)

Les fonctions de fichiers de gestion de réseau permettent de surveiller et de fermer les ressources de fichier, de périphérique et de canal ouvertes sur un serveur. Les fonctions de fichier sont répertoriées ci-dessous.



| Fonction                                | Description                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Force la fermeture d’une ressource.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Retourne des informations sur les fichiers ouverts sur un serveur.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Retourne des informations sur une ouverture particulière d’une ressource de serveur. |



 

Appelez la fonction [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) lorsque le fichier ne peut pas être fermé par un autre moyen. Cette fonction doit être utilisée avec précaution, car **NetFileClose** n’écrit pas les données mises en cache sur le système client dans le fichier avant de fermer le fichier.

La fonction [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) retourne des informations sur les ressources ouvertes sur un serveur. Un fichier peut être ouvert une ou plusieurs fois par une ou plusieurs applications. Chaque ouverture de fichier est identifiée de manière unique. La fonction **NetFileEnum** retourne une entrée pour chaque ouverture de fichier. La fonction [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) retourne des informations sur l’ouverture d’une ressource.

Les informations de fichier sont disponibles aux niveaux suivants :

-   [**\_Informations sur le fichier \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [**\_Informations sur le fichier \_ 3**](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

Les niveaux 0 et 1 ne sont pas pris en charge. Le niveau 2 retourne uniquement le numéro d’identification affecté à la ressource lors de son ouverture. Le niveau 3 retourne le numéro d’identification, les autorisations, les verrous de fichier et le nom de l’utilisateur qui a ouvert la ressource.

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) et [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) . Pour plus d’informations, consultez [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) et [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
