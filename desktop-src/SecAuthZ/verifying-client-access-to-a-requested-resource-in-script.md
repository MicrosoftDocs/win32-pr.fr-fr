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
ms.openlocfilehash: 7393001c63f0a5b605870a8498e76231f0bf620a8c7e819a8c624eace565499a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906699"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Vérification de l’accès client aux ressources demandées dans le script

Appelez la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) pour vérifier si le client a accès à une ou plusieurs opérations. Pour plus d’informations sur la création d’un objet **IAzClientContext** , consultez [la rubrique établissement d’un contexte client dans un script](establishing-a-client-context-in-script.md).

Un client peut être membre de plusieurs rôles, et une opération peut être assignée à plusieurs tâches, de sorte que le gestionnaire d’autorisations vérifie tous les rôles et toutes les tâches. Si un rôle auquel appartient le client contient une tâche qui contient une opération, l’accès à cette opération est accordé.

Pour vérifier l’accès à un seul rôle auquel le client appartient, définissez la propriété [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) de l’objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .

Lors de l’initialisation du magasin de stratégies d’autorisation pour la vérification de l’accès, vous devez passer zéro comme valeur du paramètre *lFlags* de la méthode [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) de l’objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .

Il est également possible d’appliquer une logique métier au moment de l’exécution pour qualifier l’accès. Pour plus d’informations sur l’accès éligible avec la logique métier, consultez [qualifier l’accès avec la logique métier dans le script](qualifying-access-with-business-logic-in-script.md).

L’exemple suivant montre comment vérifier l’accès d’un client à une opération. L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée Expense et une opération nommée UseFormControl.


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



 

 



