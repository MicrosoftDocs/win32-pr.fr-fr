---
title: Chargement et inscription d’une bibliothèque de types
description: La bibliothèque de liens dynamiques Automation, Oleaut32.dll, fournit plusieurs fonctions que vous pouvez appeler pour charger et inscrire une bibliothèque de types. L’appel de LoadTypeLibEx, comme indiqué dans l’exemple suivant, charge la bibliothèque et crée les entrées de registre.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854229"
---
# <a name="loading-and-registering-a-type-library"></a>Chargement et inscription d’une bibliothèque de types

La bibliothèque de liens dynamiques Automation, Oleaut32.dll, fournit plusieurs fonctions que vous pouvez appeler pour charger et inscrire une bibliothèque de types. L’appel de [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), comme indiqué dans l’exemple suivant, charge la bibliothèque et crée les entrées de registre.

## <a name="example"></a>Exemple

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

 

 