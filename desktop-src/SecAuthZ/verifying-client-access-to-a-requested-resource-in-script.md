---
description: 'Appelez la méthode IAzClientContext :: AccessCheck pour vérifier si le client a accès à une ou plusieurs opérations.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Vérification de l’accès client aux ressources demandées dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521259"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="4d092-103">Vérification de l’accès client aux ressources demandées dans le script</span><span class="sxs-lookup"><span data-stu-id="4d092-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="4d092-104">Appelez la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) pour vérifier si le client a accès à une ou plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="4d092-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="4d092-105">Pour plus d’informations sur la création d’un objet **IAzClientContext** , consultez [la rubrique établissement d’un contexte client dans un script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="4d092-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="4d092-106">Un client peut être membre de plusieurs rôles, et une opération peut être assignée à plusieurs tâches, de sorte que le gestionnaire d’autorisations vérifie tous les rôles et toutes les tâches.</span><span class="sxs-lookup"><span data-stu-id="4d092-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="4d092-107">Si un rôle auquel appartient le client contient une tâche qui contient une opération, l’accès à cette opération est accordé.</span><span class="sxs-lookup"><span data-stu-id="4d092-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="4d092-108">Pour vérifier l’accès à un seul rôle auquel le client appartient, définissez la propriété [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) de l’objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="4d092-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="4d092-109">Lors de l’initialisation du magasin de stratégies d’autorisation pour la vérification de l’accès, vous devez passer zéro comme valeur du paramètre *lFlags* de la méthode [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) de l’objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="4d092-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="4d092-110">Il est également possible d’appliquer une logique métier au moment de l’exécution pour qualifier l’accès.</span><span class="sxs-lookup"><span data-stu-id="4d092-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="4d092-111">Pour plus d’informations sur l’accès éligible avec la logique métier, consultez [qualifier l’accès avec la logique métier dans le script](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="4d092-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="4d092-112">L’exemple suivant montre comment vérifier l’accès d’un client à une opération.</span><span class="sxs-lookup"><span data-stu-id="4d092-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="4d092-113">L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée Expense et une opération nommée UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="4d092-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


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

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



