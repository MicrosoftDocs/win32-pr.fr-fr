---
title: Fonctions de groupe
description: Un groupe global contient des comptes d’utilisateurs d’un domaine qui sont regroupés sous un nom de compte de groupe.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009407"
---
# <a name="group-functions"></a>Fonctions de groupe

Un *groupe global* contient des comptes d’utilisateurs d’un domaine qui sont regroupés sous un nom de compte de groupe. Un groupe global peut contenir uniquement des membres (utilisateurs) du domaine dans lequel le groupe global est créé ; il ne peut pas contenir de groupes locaux. Un groupe global est disponible dans son propre domaine et dans n’importe quel domaine d’approbation.

Les fonctions de groupe d’administration de réseau contrôlent les groupes globaux. Les fonctions de groupe sont répertoriées ci-dessous.



| Fonction                                     | Description                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crée un groupe global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Ajoute un utilisateur à un groupe global existant.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Supprime un groupe global, que le groupe ait ou non des membres.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Supprime un nom d’utilisateur d’un groupe global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Répertorie tous les groupes globaux sur un serveur.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Retourne des informations sur un groupe global particulier.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Répertorie tous les membres d’un groupe global particulier.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Définit des informations générales sur un groupe global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Attribue des membres à un nouveau groupe global ; remplace les membres d’un groupe existant. |



 

Quand vous appelez la fonction [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) pour créer un groupe global, vous devez fournir un nom de groupe. Au départ, un nouveau groupe n’a aucun membre.

Les comptes d’utilisateurs appartiennent automatiquement aux utilisateurs du domaine de groupe global spécial. L’appartenance à ce groupe est indirectement contrôlée par les fonctions [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)et [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .

Les informations de compte de groupe global sont disponibles aux niveaux suivants :

-   [**Infos de groupe \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**\_Infos sur le groupe \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**\_Informations sur le groupe \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**\_Infos sur le groupe \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**\_Informations sur le groupe \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**\_Informations sur le groupe \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

Les niveaux 1002 et 1005 sont valides uniquement pour la fonction [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .

Les informations des membres du groupe global sont disponibles au niveau des informations suivantes :

-   [**\_Informations sur les utilisateurs du groupe \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Pour plus d’informations, consultez fonctions de [groupe local](local-group-functions.md)de gestion de réseau.

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de groupe d’administration réseau. Pour plus d’informations, consultez [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 