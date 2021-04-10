---
description: Pour établir un contexte client dans le script, une application peut créer un contexte client avec un handle vers un jeton, un domaine et un nom d’utilisateur, ou une représentation sous forme de chaîne de l’identificateur de sécurité du client.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Établissement d’un contexte client dans un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867222"
---
# <a name="establishing-a-client-context-in-script"></a>Établissement d’un contexte client dans un script

Dans le gestionnaire d’autorisations, une application détermine si un client est autorisé à accéder à une opération en appelant la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , qui représente un contexte client.

Une application peut créer un contexte client avec un handle vers un jeton, un domaine et un nom d’utilisateur, ou une représentation sous forme de chaîne de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du client.

Utilisez les méthodes [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)et [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) d’un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) pour créer un contexte client.

L’exemple suivant montre comment créer un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) à partir d’un nom de client. L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée expense.


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

%>
```



 

 
