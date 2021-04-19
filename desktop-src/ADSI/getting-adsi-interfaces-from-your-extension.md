---
title: Obtention des interfaces ADSI à partir de votre extension
description: Une extension doit souvent recevoir des données de l’objet annuaire auquel elle est liée.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- extensions ADSI, obtention des interfaces ADSI à partir de votre extension
- ADSI ADSI, exemple de code C/C++, obtention des interfaces ADSI à partir de votre extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509062"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="a06bd-105">Obtention des interfaces ADSI à partir de votre extension</span><span class="sxs-lookup"><span data-stu-id="a06bd-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="a06bd-106">Une extension doit souvent recevoir des données de l’objet annuaire auquel elle est liée.</span><span class="sxs-lookup"><span data-stu-id="a06bd-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="a06bd-107">Par exemple, une extension pour un objet **ordinateur** peut vouloir obtenir le **dNSHostName** de l’objet actuel à partir de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a06bd-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="a06bd-108">Cela peut être facilement effectué en émettant un appel **QueryInterface** sur l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="a06bd-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



<span data-ttu-id="a06bd-109">Vous devez libérer l’interface immédiatement après l’avoir utilisée.</span><span class="sxs-lookup"><span data-stu-id="a06bd-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="a06bd-110">Si l’extension a une référence ouverte à l’agrégation, vous avez créé une référence circulaire et l’agrégation ne peut pas libérer l’extension.</span><span class="sxs-lookup"><span data-stu-id="a06bd-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="a06bd-111">Par conséquent, l’agrégation ne peut pas être libérée et le résultat est une fuite de mémoire dans votre application.</span><span class="sxs-lookup"><span data-stu-id="a06bd-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 