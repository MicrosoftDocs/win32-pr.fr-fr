---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "106529230"
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
