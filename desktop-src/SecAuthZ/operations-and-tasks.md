---
description: Une opération est une action d’ordinateur de bas niveau.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Opérations et tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013685"
---
# <a name="operations-and-tasks"></a>Opérations et tâches

Une opération est une action d’ordinateur de bas niveau. Dans l’API du gestionnaire d’autorisations, une opération est représentée par un objet [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . En général, les opérations sont trop nombreuses et trop faibles pour faciliter l’administration. Regroupez les opérations dans des tâches pour simplifier l’administration de la stratégie d’autorisation.

Une tâche est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) et peut contenir un ou plusieurs objets [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Un objet **IAzTask** peut également contenir d’autres objets **IAzTask** , afin que les tâches puissent être imbriquées. Pour faciliter l’administration, un objet **IAzTask** doit représenter une tâche qu’un utilisateur réel souhaite effectuer.

L’accès aux opérations contenues par une tâche peut être qualifié au moment de l’exécution par un script de règle d’entreprise associé à l’objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) qui représente cette tâche. Pour plus d’informations sur les scripts de règle d’entreprise, consultez [Business Rules](business-rules.md).

Un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) peut également représenter une définition de rôle en affectant à sa propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) la **valeur true**. L’interface utilisateur du composant logiciel enfichable MMC du **Gestionnaire d’autorisations** affiche ensuite cet objet **IAzTask** en tant que rôle. Pour plus d’informations sur les définitions de rôles, consultez [rôles](roles.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition d’opérations en C++](defining-operations-in-c--.md)
</dt> <dt>

[Regroupement d’opérations en tâches en C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Regroupement de tâches en rôles en C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Utilisateurs et groupes](users-and-groups.md)
</dt> </dl>

 

 



