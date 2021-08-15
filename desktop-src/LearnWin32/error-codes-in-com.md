---
title: Codes d’erreur dans COM
description: Codes d’erreur dans COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dd61208c9ae825999ec0dec024a8cc492b81cae426b1cc4143d694034204d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388287"
---
# <a name="error-codes-in-com"></a>Codes d’erreur dans COM

Pour indiquer la réussite ou l’échec, les méthodes et les fonctions COM retournent une valeur de type **HRESULT**. Un **HRESULT** est un entier 32 bits. Le bit de poids fort de la valeur **HRESULT** signale la réussite ou l’échec. Zéro (0) indique une réussite et 1 indique un échec.

Cela produit les plages numériques suivantes :

-   Codes de réussite : 0x0 – 0x7FFFFFFF.
-   Codes d’erreur : 0x80000000 – 0xFFFFFFFF.

Un petit nombre de méthodes COM ne retournent pas de valeur **HRESULT** . Par exemple, les méthodes [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) retournent des valeurs long non signées. Toutefois, chaque méthode COM qui retourne un code d’erreur en retournant une valeur **HRESULT** .

Pour vérifier si une méthode COM est réussie, examinez le bit de poids fort de la valeur **HRESULT** retournée. les en-têtes SDK Windows fournissent deux macros qui facilitent cette opération : la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) et la macro qui [**a échoué**](/windows/desktop/api/winerror/nf-winerror-failed) . La macro **Succeeded** retourne la **valeur true** si un **HRESULT** est un code de réussite et **false** s’il s’agit d’un code d’erreur. L’exemple suivant vérifie si [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) est correctement effectué.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



Il est parfois plus pratique de tester la condition inverse. La macro [**ayant échoué**](/windows/desktop/api/winerror/nf-winerror-failed) fait l’inverse de la [**réussite**](/windows/desktop/api/winerror/nf-winerror-succeeded). Elle retourne **true** pour un code d’erreur et **false** pour un code de réussite.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Plus loin dans ce module, nous examinerons quelques conseils pratiques sur la façon de structurer votre code pour gérer les erreurs COM. (Voir [gestion des erreurs dans com](error-handling-in-com.md).)

## <a name="next"></a>Suivant

[Création d’un objet dans COM](creating-an-object-in-com.md)

 

 
