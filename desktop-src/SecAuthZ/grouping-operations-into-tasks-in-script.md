---
description: Dans le gestionnaire d’autorisations, une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Regroupement d’opérations en tâches dans un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29c7dedb9944a208e5ba128f0341a8cbde3e787056c099d527be8f79260c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913573"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Regroupement d’opérations en tâches dans un script

Dans le gestionnaire d’autorisations, une tâche est une action de haut niveau que les utilisateurs d’une application doivent effectuer. Les tâches sont constituées d’opérations, qui sont des fonctions de bas niveau et des méthodes de l’application. Une tâche est ensuite affectée aux rôles qui doivent effectuer cette tâche. Une tâche est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Pour plus d’informations sur les opérations et les tâches, consultez [opérations et tâches](operations-and-tasks.md).

L’exemple suivant montre comment regrouper des opérations pour créer une tâche. L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, que ce magasin contient une application nommée Expense et que cette application contient des opérations définies dans la rubrique [définition d’opérations dans le script](defining-operations-in-script.md).


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



