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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096102"
---
# <a name="creating-an-application-object-in-script"></a>Création d’un objet d’application dans un script

Un magasin de stratégies d’autorisation contient des informations de stratégie d’autorisation pour une ou plusieurs applications. Pour chaque application qui utilise un magasin de stratégies d’autorisation, vous devez créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) et l’enregistrer dans un magasin de stratégies.

L’exemple suivant montre comment créer un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui représente une application et comment ajouter l’objet **IAzApplication** au magasin de stratégies d’autorisation utilisé par l’application. L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.


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



 

 



