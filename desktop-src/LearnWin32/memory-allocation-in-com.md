---
title: Allocation de mémoire dans COM
description: Allocation de mémoire dans COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a38477f0db860cf768493417470f2da3395e814bc106cf85f975ed11ba2c0b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979979"
---
# <a name="memory-allocation-in-com"></a>Allocation de mémoire dans COM

Parfois, une méthode alloue une mémoire tampon sur le tas et retourne l’adresse de la mémoire tampon à l’appelant. COM définit une paire de fonctions pour allouer et libérer de la mémoire sur le tas.

-   La fonction [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alloue un bloc de mémoire.
-   La fonction [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libère un bloc de mémoire qui a été alloué avec [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Nous avons vu un exemple de ce modèle dans l' [exemple de boîte de dialogue Ouvrir](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



La méthode [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) alloue de la mémoire pour une chaîne. En interne, la méthode appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer la chaîne. Lorsque la méthode retourne, *pszFilePath* pointe vers l’emplacement de mémoire de la nouvelle mémoire tampon. L’appelant est chargé d’appeler [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire.

Pourquoi COM définit-il ses propres fonctions d’allocation de mémoire ? L’une des raisons est de fournir une couche d’abstraction sur l’allocateur de tas. Dans le cas contraire, certaines méthodes peuvent appeler **malloc** , tandis que d’autres ont appelé **New**. Ensuite, votre programme doit appeler **Free** dans certains cas et le **supprimer** dans d’autres, et le suivi de tout cela deviendrait rapidement impossible. Les fonctions d’allocation COM créent une approche uniforme.

Un autre point à prendre en compte est le fait que COM est une norme *binaire* , donc il n’est pas lié à un langage de programmation particulier. Par conséquent, COM ne peut pas reposer sur une forme d’allocation de mémoire propre au langage.

## <a name="next"></a>Suivant

[Pratiques de codage COM](com-coding-practices.md)

 

 
