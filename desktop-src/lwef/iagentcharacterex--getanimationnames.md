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
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="94a62-103">IAgentCharacterEx::GetAnimationNames</span><span class="sxs-lookup"><span data-stu-id="94a62-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="94a62-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94a62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="94a62-105">Récupère les noms d’animation d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="94a62-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="94a62-106">Retourne la valeur **S \_ OK** pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="94a62-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="94a62-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="94a62-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="94a62-108">Adresse de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour la collection d’animations du caractère.</span><span class="sxs-lookup"><span data-stu-id="94a62-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="94a62-109">Cette fonction vous permet d’énumérer les noms des animations d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="94a62-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="94a62-110">Les éléments de la collection n’ont pas de propriétés, donc les éléments individuels ne sont pas accessibles directement.</span><span class="sxs-lookup"><span data-stu-id="94a62-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="94a62-111">Pour accéder à la collection, interrogez punkEnum pour l’interface IEnumVARIANT :</span><span class="sxs-lookup"><span data-stu-id="94a62-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


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
> <span data-ttu-id="94a62-112">Pour les caractères ACF, la collection retourne toutes les animations qui ont été définies pour le caractère, en ajoutant à celles qui ont été récupérées avec la méthode d' [**extraction**](https://www.bing.com/search?q=**Get**) .</span><span class="sxs-lookup"><span data-stu-id="94a62-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
