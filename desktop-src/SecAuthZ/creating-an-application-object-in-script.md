---
description: Pour chaque application qui utilise un magasin de stratégies d’autorisation, vous devez créer un objet IAzApplication, puis l’enregistrer dans un magasin de stratégies.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Création d’un objet d’application dans un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753493"
---
# <a name="creating-an-application-object-in-script"></a><span data-ttu-id="fb8a2-103">Création d’un objet d’application dans un script</span><span class="sxs-lookup"><span data-stu-id="fb8a2-103">Creating an Application Object in Script</span></span>

<span data-ttu-id="fb8a2-104">Un magasin de stratégies d’autorisation contient des informations de stratégie d’autorisation pour une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="fb8a2-104">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="fb8a2-105">Pour chaque application qui utilise un magasin de stratégies d’autorisation, vous devez créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) et l’enregistrer dans un magasin de stratégies.</span><span class="sxs-lookup"><span data-stu-id="fb8a2-105">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>

<span data-ttu-id="fb8a2-106">L’exemple suivant montre comment créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui représente une application et comment ajouter l’objet **IAzApplication** au magasin de stratégies d’autorisation utilisé par l’application.</span><span class="sxs-lookup"><span data-stu-id="fb8a2-106">The following example shows how to create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that represents an application and how to add the **IAzApplication** object to the authorization policy store the application uses.</span></span> <span data-ttu-id="fb8a2-107">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.</span><span class="sxs-lookup"><span data-stu-id="fb8a2-107">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



