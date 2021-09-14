---
title: Fonctions de groupe locales
description: Un groupe local peut contenir des comptes d’utilisateurs ou des comptes de groupes globaux d’un ou plusieurs domaines. (Les groupes globaux peuvent contenir des utilisateurs d’un seul domaine.) Un groupe local partage des privilèges et des droits communs uniquement dans son propre domaine.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009403"
---
# <a name="local-group-functions"></a>Fonctions de groupe locales

Un *groupe local* peut contenir des comptes d’utilisateurs ou des comptes de groupes globaux d’un ou plusieurs domaines. (Les groupes globaux peuvent contenir des utilisateurs d’un seul domaine.) Un groupe local partage des privilèges et des droits communs uniquement dans son propre domaine.

Les fonctions de groupe local de gestion de réseau contrôlent les membres des groupes locaux de telle sorte que les fonctions ne peuvent être appelées que localement sur le système sur lequel le groupe local est défini. Sur une station de travail ou sur un serveur qui n’est pas un contrôleur de domaine, vous pouvez utiliser uniquement un groupe local défini sur ce système.

Dans Active Directory, les domaines en mode natif, les groupes locaux sont appelés *groupes locaux de domaine*. Les groupes locaux de domaine sont disponibles sur tous les contrôleurs de domaine, les serveurs membres et les stations de travail joints au domaine. Active Directory domaines en mode mixte sont définis sur le contrôleur de domaine principal et répliqués sur tous les autres contrôleurs de domaine du domaine. Par conséquent, un groupe local est disponible sur tous les contrôleurs de domaine dans le domaine dans lequel il a été créé.

Les fonctions de groupe local créent ou suppriment des groupes locaux, et vérifient ou ajustent les appartenances aux groupes locaux. Ces fonctions sont répertoriées ci-dessous.



| Fonction                                                   | Description                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crée un groupe local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Ajoute un ou plusieurs utilisateurs ou groupes globaux à un groupe local existant.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Supprime un groupe local, en supprimant tous les membres existants du groupe.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Supprime un ou plusieurs membres d’un groupe local existant.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Retourne des informations sur chaque compte de groupe local sur un serveur.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Retourne des informations sur un compte de groupe local particulier sur un serveur. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Répertorie tous les membres d’un groupe local spécifié.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Définit des informations générales sur un groupe local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Attribue des membres à un groupe local.                                       |



 

Vous pouvez ajouter un membre à un groupe local en spécifiant l’identificateur de sécurité (SID) du membre. Pour convertir un nom de compte de membre en SID, appelez la fonction [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .

Lorsque vous créez un groupe local en appelant la fonction [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) , vous devez fournir un nom de groupe local. Au départ, le groupe local n’a aucun membre.

Les informations de compte de groupe local sont disponibles aux niveaux suivants :

-   [**\_Infos localgroup \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**\_Infos localgroup \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**\_Infos LOCALGROUP \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

Les informations d’appartenance au groupe local sont disponibles aux niveaux d’informations suivants :

-   [**\_Informations sur les membres du localgroup \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**\_Informations sur les membres du localgroup \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**\_Informations sur les membres du localgroup \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**\_Informations sur les membres du localgroup \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

Vous pouvez récupérer les noms des groupes locaux auxquels appartient un utilisateur en appelant la fonction [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) , en spécifiant le niveau d’information suivant :

[**\_Informations sur les utilisateurs de l’utilisateur local \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Pour plus d’informations, consultez fonctions de [groupe](group-functions.md)d’administration réseau.

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de groupe local de gestion de réseau. Pour plus d’informations, consultez [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 