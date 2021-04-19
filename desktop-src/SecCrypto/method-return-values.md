---
description: La valeur de retour pour les méthodes d’interface C++ est toujours de type HRESULT ; Cette valeur peut être vérifiée pour déterminer la réussite ou l’échec.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valeurs de retour de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514034"
---
# <a name="method-return-values"></a><span data-ttu-id="cb0a5-103">Valeurs de retour de méthode</span><span class="sxs-lookup"><span data-stu-id="cb0a5-103">Method Return Values</span></span>

<span data-ttu-id="cb0a5-104">La valeur de retour pour les méthodes d’interface C++ est toujours de type **HRESULT**; Cette valeur peut être vérifiée pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="cb0a5-105">L’utilisation de paramètres de « sortie » permet d’assigner des valeurs à des variables pendant l’appel de la méthode ou de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="cb0a5-106">L’exemple suivant illustre un appel de méthode C++ pour énumérer des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="cb0a5-107">Dans le fragment de code précédent, la réussite ou l’échec est retourné à la variable « hr ».</span><span class="sxs-lookup"><span data-stu-id="cb0a5-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="cb0a5-108">Si l’appel a réussi, HR est défini sur S \_ OK et la variable bstrProvider contient le nom du fournisseur énuméré.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="cb0a5-109">Un appel C++ pour récupérer une valeur de propriété serait le suivant.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="cb0a5-110">Un appel C++ pour définir une valeur de propriété serait le suivant.</span><span class="sxs-lookup"><span data-stu-id="cb0a5-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



