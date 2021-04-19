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
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516921"
---
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="9615e-103">Accès éligible avec la logique métier dans le script</span><span class="sxs-lookup"><span data-stu-id="9615e-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="9615e-104">Utilisez des scripts de règle d’entreprise pour fournir une logique d’exécution pour la vérification de l’accès.</span><span class="sxs-lookup"><span data-stu-id="9615e-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="9615e-105">Pour plus d’informations sur les règles d’entreprise, consultez [règles d’entreprise](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="9615e-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="9615e-106">Pour affecter une règle d’entreprise à une tâche, commencez par définir la propriété [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) de l’objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) qui représente la tâche.</span><span class="sxs-lookup"><span data-stu-id="9615e-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="9615e-107">Le script doit être écrit à l’aide du langage de programmation Visual Basic Scripting Edition (VBScript) ou du logiciel de développement JScript.</span><span class="sxs-lookup"><span data-stu-id="9615e-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="9615e-108">Une fois que vous avez spécifié le langage de script, définissez la propriété [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) de l’objet **IAzTask** avec une représentation sous forme de chaîne du script.</span><span class="sxs-lookup"><span data-stu-id="9615e-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="9615e-109">Lors de la vérification de l’accès à une opération contenue par une tâche associée à une règle d’entreprise, l’application doit créer deux tableaux de la même taille à transmettre en tant que paramètres *varParameterNames* et *varParameterValues* de la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="9615e-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="9615e-110">Pour plus d’informations sur la création d’un contexte client, consultez [établissement d’un contexte client dans un script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="9615e-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="9615e-111">La méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crée un objet [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) qui est transmis au script de règle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9615e-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="9615e-112">Le script définit ensuite la propriété [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) de l’objet **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="9615e-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="9615e-113">La valeur **true** indique que l’accès est accordé et la valeur **false** indique que l’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="9615e-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="9615e-114">Un script de règle d’entreprise ne peut pas être assigné à un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenu dans un objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) délégué.</span><span class="sxs-lookup"><span data-stu-id="9615e-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="9615e-115">L’exemple suivant montre comment utiliser un script de règle d’entreprise pour vérifier l’accès d’un client à une opération.</span><span class="sxs-lookup"><span data-stu-id="9615e-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="9615e-116">L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée Expense, une tâche nommée Submit Expense et une opération nommée UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="9615e-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



