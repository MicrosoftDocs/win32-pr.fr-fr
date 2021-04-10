---
title: Chargement et inscription d’une bibliothèque de types
description: La bibliothèque de liens dynamiques Automation, Oleaut32.dll, fournit plusieurs fonctions que vous pouvez appeler pour charger et inscrire une bibliothèque de types. L’appel de LoadTypeLibEx, comme indiqué dans l’exemple suivant, charge la bibliothèque et crée les entrées de registre.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031972"
---
# <a name="loading-and-registering-a-type-library"></a><span data-ttu-id="289c1-104">Chargement et inscription d’une bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="289c1-104">Loading and Registering a Type Library</span></span>

<span data-ttu-id="289c1-105">La bibliothèque de liens dynamiques Automation, Oleaut32.dll, fournit plusieurs fonctions que vous pouvez appeler pour charger et inscrire une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="289c1-105">The Automation dynamic link library, Oleaut32.dll, provides several functions that you can call to load and register a type library.</span></span> <span data-ttu-id="289c1-106">L’appel de [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), comme indiqué dans l’exemple suivant, charge la bibliothèque et crée les entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="289c1-106">Calling [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), as shown in the following example, both loads the library and creates the registry entries.</span></span>

## <a name="example"></a><span data-ttu-id="289c1-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="289c1-107">Example</span></span>

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 