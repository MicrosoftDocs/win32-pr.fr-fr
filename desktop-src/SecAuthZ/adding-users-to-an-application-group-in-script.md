---
description: Un groupe d’applications est un groupe d’utilisateurs et de groupes d’utilisateurs. Comme un groupe d’applications peut contenir d’autres groupes d’applications, les groupes d’utilisateurs peuvent être imbriqués. Un groupe d’applications est représenté par un objet IAzApplicationGroup.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Ajout d’utilisateurs à un groupe d’applications dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528266"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="a490f-105">Ajout d’utilisateurs à un groupe d’applications dans le script</span><span class="sxs-lookup"><span data-stu-id="a490f-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="a490f-106">Dans le gestionnaire d’autorisations, un groupe d’applications est un groupe d’utilisateurs et de groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a490f-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="a490f-107">Comme un groupe d’applications peut contenir d’autres groupes d’applications, les groupes d’utilisateurs peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="a490f-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="a490f-108">Un groupe d’applications est représenté par un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="a490f-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="a490f-109">**Pour permettre aux membres d’un groupe d’applications d’effectuer une tâche ou un ensemble de tâches**</span><span class="sxs-lookup"><span data-stu-id="a490f-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="a490f-110">Affectez ce groupe d’applications à un rôle qui contient ces tâches.</span><span class="sxs-lookup"><span data-stu-id="a490f-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="a490f-111">Les rôles sont représentés par des objets [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="a490f-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="a490f-112">L’exemple suivant montre comment créer un groupe d’applications, ajouter un utilisateur en tant que membre du groupe d’applications et affecter le groupe d’applications à un rôle existant.</span><span class="sxs-lookup"><span data-stu-id="a490f-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="a490f-113">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, que ce magasin contient une application nommée Expense et que cette application contient un rôle nommé administrateur des dépenses.</span><span class="sxs-lookup"><span data-stu-id="a490f-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



