---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478025"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx::GetAnimationNames

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Récupère les noms d’animation d’un caractère.

-   Retourne la valeur **S \_ OK** pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Adresse de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour la collection d’animations du caractère.

</dd> </dl>

Cette fonction vous permet d’énumérer les noms des animations d’un caractère. Les éléments de la collection n’ont pas de propriétés, donc les éléments individuels ne sont pas accessibles directement. Pour accéder à la collection, interrogez punkEnum pour l’interface IEnumVARIANT :


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> Pour les caractères ACF, la collection retourne toutes les animations qui ont été définies pour le caractère, en ajoutant à celles qui ont été récupérées avec la méthode d' [**extraction**](https://www.bing.com/search?q=**Get**) .
