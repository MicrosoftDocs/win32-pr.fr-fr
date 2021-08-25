---
description: Utilisation de scripts de règle d’entreprise dans le script pour fournir une logique d’exécution pour la vérification de l’accès.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Accès éligible avec la logique métier dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b77ff1d6d520780d30efab5619c3e9bc3c896ad88315fba56e3a19e05d3ae97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907549"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Accès éligible avec la logique métier dans le script

Utilisez des scripts de règle d’entreprise pour fournir une logique d’exécution pour la vérification de l’accès. Pour plus d’informations sur les règles d’entreprise, consultez [règles d’entreprise](business-rules.md).

Pour affecter une règle d’entreprise à une tâche, commencez par définir la propriété [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) de l’objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) qui représente la tâche. le script doit être écrit à l’aide du langage de programmation VBScript (Visual Basic scripting Edition) ou JScript logiciel de développement. Une fois que vous avez spécifié le langage de script, définissez la propriété [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) de l’objet **IAzTask** avec une représentation sous forme de chaîne du script.

Lors de la vérification de l’accès à une opération contenue par une tâche associée à une règle d’entreprise, l’application doit créer deux tableaux de la même taille à transmettre en tant que paramètres *varParameterNames* et *varParameterValues* de la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) . Pour plus d’informations sur la création d’un contexte client, consultez [établissement d’un contexte client dans un script](establishing-a-client-context-in-script.md).

La méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crée un objet [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) qui est transmis au script de règle d’entreprise. Le script définit ensuite la propriété [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) de l’objet **AzBizRuleContext** . La valeur **true** indique que l’accès est accordé et la valeur **false** indique que l’accès est refusé.

Un script de règle d’entreprise ne peut pas être assigné à un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenu dans un objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) délégué.

L’exemple suivant montre comment utiliser un script de règle d’entreprise pour vérifier l’accès d’un client à une opération. L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée Expense, une tâche nommée Submit Expense et une opération nommée UseFormControl.


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



