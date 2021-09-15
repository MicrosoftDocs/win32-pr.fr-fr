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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311326"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Regroupement de tâches en rôles dans le script

Dans le gestionnaire d’autorisations, un rôle représente une catégorie d’utilisateurs et les tâches que ces utilisateurs sont autorisés à effectuer. Les tâches sont regroupées et affectées à une définition de rôle, qui est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) avec la propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) définie sur **true**. La définition de rôle peut ensuite être assignée à un objet [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , et les utilisateurs ou groupes d’utilisateurs sont ensuite attribués à cet objet. Pour plus d’informations sur les tâches et les rôles, consultez [rôles](roles.md).

L’exemple suivant montre comment assigner des tâches à une définition de rôle, créer un objet Role et affecter la définition de rôle à l’objet Role. L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, que ce magasin contient une application nommée Expense et que cette application contient des tâches nommées envoyer des dépenses et approuver les dépenses.


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



 

 



