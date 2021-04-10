---
description: Dans le gestionnaire d’autorisations, un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Regroupement de tâches en rôles dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952786"
---
# <a name="grouping-tasks-into-roles-in-script"></a><span data-ttu-id="2859f-103">Regroupement de tâches en rôles dans le script</span><span class="sxs-lookup"><span data-stu-id="2859f-103">Grouping Tasks into Roles in Script</span></span>

<span data-ttu-id="2859f-104">Dans le gestionnaire d’autorisations, un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2859f-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="2859f-105">Les tâches sont regroupées et affectées à une définition de rôle, qui est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) avec la propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="2859f-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **True**.</span></span> <span data-ttu-id="2859f-106">La définition de rôle peut ensuite être assignée à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , et les utilisateurs ou groupes d’utilisateurs sont ensuite attribués à cet objet.</span><span class="sxs-lookup"><span data-stu-id="2859f-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="2859f-107">Pour plus d’informations sur les tâches et les rôles, consultez [rôles](roles.md).</span><span class="sxs-lookup"><span data-stu-id="2859f-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="2859f-108">L’exemple suivant montre comment assigner des tâches à une définition de rôle, créer un objet Role et affecter la définition de rôle à l’objet Role.</span><span class="sxs-lookup"><span data-stu-id="2859f-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="2859f-109">L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, que ce magasin contient une application nommée Expense et que cette application contient des tâches nommées envoyer des dépenses et approuver les dépenses.</span><span class="sxs-lookup"><span data-stu-id="2859f-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



