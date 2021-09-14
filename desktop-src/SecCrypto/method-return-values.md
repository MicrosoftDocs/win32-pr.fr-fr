---
description: La valeur de retour pour les méthodes d’interface C++ est toujours de type HRESULT ; Cette valeur peut être vérifiée pour déterminer la réussite ou l’échec.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valeurs de retour de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237491"
---
# <a name="method-return-values"></a>Valeurs de retour de méthode

La valeur de retour pour les méthodes d’interface C++ est toujours de type **HRESULT**; Cette valeur peut être vérifiée pour déterminer la réussite ou l’échec. L’utilisation de paramètres de « sortie » permet d’assigner des valeurs à des variables pendant l’appel de la méthode ou de la propriété. L’exemple suivant illustre un appel de méthode C++ pour énumérer des fournisseurs.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



Dans le fragment de code précédent, la réussite ou l’échec est retourné à la variable « hr ». Si l’appel a réussi, HR est défini sur S \_ OK et la variable bstrProvider contient le nom du fournisseur énuméré.

Un appel C++ pour récupérer une valeur de propriété serait le suivant.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Un appel C++ pour définir une valeur de propriété serait le suivant.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



