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
# <a name="establishing-a-client-context-in-script"></a><span data-ttu-id="d0363-103">Établissement d’un contexte client dans un script</span><span class="sxs-lookup"><span data-stu-id="d0363-103">Establishing a Client Context in Script</span></span>

<span data-ttu-id="d0363-104">Dans le gestionnaire d’autorisations, une application détermine si un client est autorisé à accéder à une opération en appelant la méthode [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) d’un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , qui représente un contexte client.</span><span class="sxs-lookup"><span data-stu-id="d0363-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="d0363-105">Une application peut créer un contexte client avec un handle vers un jeton, un domaine et un nom d’utilisateur, ou une représentation sous forme de chaîne de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du client.</span><span class="sxs-lookup"><span data-stu-id="d0363-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="d0363-106">Utilisez les méthodes [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)et [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) d’un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) pour créer un contexte client.</span><span class="sxs-lookup"><span data-stu-id="d0363-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object to create a client context.</span></span>

<span data-ttu-id="d0363-107">L’exemple suivant montre comment créer un objet [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) à partir d’un nom de client.</span><span class="sxs-lookup"><span data-stu-id="d0363-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client name.</span></span> <span data-ttu-id="d0363-108">L’exemple suppose qu’il existe un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C, et que ce magasin contient une application nommée expense.</span><span class="sxs-lookup"><span data-stu-id="d0363-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


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



 

 
