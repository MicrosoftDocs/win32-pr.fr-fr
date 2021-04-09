---
description: Les rôles ont deux objectifs différents dans le gestionnaire d’autorisations.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Rôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863018"
---
# <a name="roles"></a>Rôles

Les rôles ont deux objectifs différents dans le gestionnaire d’autorisations. Un rôle est un ensemble de tâches ou d’opérations auxquelles une catégorie d’utilisateurs a besoin d’accéder, et il s’agit également d’un ensemble d’utilisateurs et de groupes qui tiennent dans cette catégorie.

-   [Rôles en tant qu’ensembles de tâches](#roles-as-sets-of-tasks)
-   [Rôles sous forme d’ensembles d’utilisateurs et de groupes](#roles-as-sets-of-users-and-groups)
-   [Rubriques connexes](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Rôles en tant qu’ensembles de tâches

Une stratégie d’autorisation affecte des objets [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) pour créer des ensembles de tâches. Tous les utilisateurs et groupes attribués à cet objet **IAzRole** sont ensuite autorisés à accéder à toutes les opérations contenues par ces objets **IAzTask** .

Étant donné qu’un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) représente à la fois un ensemble de tâches et un ensemble d’utilisateurs et de groupes qui ont accès à ces tâches, le gestionnaire d’autorisations fournit un moyen de créer des définitions de rôles qui peuvent être attribuées à plusieurs objets **IAzRole** . Un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) peut contenir d’autres objets **IAzTask** . Vous pouvez ensuite utiliser cet objet **IAzTask** comme définition de rôle en l’affectant à un ou plusieurs objets **IAzRole** . Affectez la valeur **true** à la propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) de l’objet **IAzTask** pour que l’interface utilisateur du composant logiciel enfichable MMC du **Gestionnaire d’autorisations** affiche l’objet **IAzTask** en tant que rôle.

## <a name="roles-as-sets-of-users-and-groups"></a>Rôles sous forme d’ensembles d’utilisateurs et de groupes

Affectez des utilisateurs et des groupes à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) pour accorder à ces utilisateurs et groupes l’accès aux tâches assignées à cet objet **IAzRole** en appelant la méthode [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) ou [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) . Assignez des groupes d’applications existants, représentés par les objets [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , à un objet **IAzRole** en appelant la méthode [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) . Tous les utilisateurs et groupes attribués à l’objet **IAzRole** ont accès aux tâches et aux opérations affectées à ce rôle. Pour plus d’informations sur les groupes d’applications, voir [utilisateurs et groupes](users-and-groups.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Regroupement de tâches en rôles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Définition de groupes d’utilisateurs en C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Ajout d’utilisateurs à un groupe d’applications en C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



