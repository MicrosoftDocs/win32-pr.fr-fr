---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520425"
---
# <a name="saferelease"></a><span data-ttu-id="004e1-103">SafeRelease</span><span class="sxs-lookup"><span data-stu-id="004e1-103">SafeRelease</span></span>


<span data-ttu-id="004e1-104">La plupart des exemples de code de cette documentation utilisent la fonction suivante pour libérer des pointeurs d’interface COM.</span><span class="sxs-lookup"><span data-stu-id="004e1-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="004e1-105">Cette fonction n’est pas définie dans un en-tête du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="004e1-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="004e1-106">Pour utiliser cette fonction, vous devez la définir dans votre propre code.</span><span class="sxs-lookup"><span data-stu-id="004e1-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="004e1-107">Cette fonction libère le pointeur *ppT* et lui affecte la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="004e1-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="004e1-108">Une autre option consiste à utiliser une classe de pointeur intelligent, telle que **CComPtr**, qui est définie dans la Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="004e1-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="004e1-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="004e1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="004e1-110">À propos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="004e1-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="004e1-111">**IUnknown :: Release**</span><span class="sxs-lookup"><span data-stu-id="004e1-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
