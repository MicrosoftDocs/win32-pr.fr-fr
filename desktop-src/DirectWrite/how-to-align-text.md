---
title: Comment aligner du texte
description: Vous pouvez aligner du texte DirectWrite à l’aide de la méthode SetTextAlignment de l’interface IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106544503"
---
# <a name="how-to-align-text"></a><span data-ttu-id="7d6a1-103">Comment aligner du texte</span><span class="sxs-lookup"><span data-stu-id="7d6a1-103">How to Align Text</span></span>

<span data-ttu-id="7d6a1-104">Vous pouvez aligner le texte [DirectWrite](direct-write-portal.md) à l’aide de la méthode [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , comme indiqué dans le code suivant qui centre le texte.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="7d6a1-105">Le texte peut être aligné sur le bord de début ou de fin de la zone de disposition, ou il peut être centré.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="7d6a1-106">L’illustration suivante montre le texte dont l’alignement est défini sur [**DWRITE \_ alignement du texte à \_ \_ gauche**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE \_ \_ \_ Centre d’alignement**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)du texte et [**DWRITE alignement du texte à \_ \_ \_ droite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivement.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![illustration des paragraphes de texte avec alignement de début, de centre et de fin](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="7d6a1-108">L’alignement dépend de la direction de lecture, ce qui précède le sens de lecture de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="7d6a1-109">Pour le sens de lecture de droite à gauche, il s’agit de l’inverse.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="7d6a1-110">Un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilise l’alignement qui a été désigné pour le [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fourni par vous lors de la création de la disposition.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="7d6a1-111">Pour modifier l’alignement du texte, utilisez [**IDWriteTextLayout :: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
