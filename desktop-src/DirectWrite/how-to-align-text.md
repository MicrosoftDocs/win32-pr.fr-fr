---
title: Comment aligner du texte
description: vous pouvez aligner DirectWrite texte à l’aide de la méthode SetTextAlignment de l’interface IDWriteTextFormat.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650363"
---
# <a name="how-to-align-text"></a>Comment aligner du texte

vous pouvez aligner [DirectWrite](direct-write-portal.md) texte à l’aide de la méthode [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , comme indiqué dans le code suivant qui centre le texte.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Le texte peut être aligné sur le bord de début ou de fin de la zone de disposition, ou il peut être centré. L’illustration suivante montre le texte dont l’alignement est défini sur [**DWRITE \_ alignement du texte à \_ \_ gauche**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE \_ \_ \_ Centre d’alignement**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)du texte et [**DWRITE alignement du texte à \_ \_ \_ droite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectivement.

![illustration des paragraphes de texte avec alignement de début, de centre et de fin](images/textalignment.png)

> [!Note]  
> L’alignement dépend de la direction de lecture, ce qui précède le sens de lecture de gauche à droite. Pour le sens de lecture de droite à gauche, il s’agit de l’inverse.

 

Un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) utilise l’alignement qui a été désigné pour le [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fourni par vous lors de la création de la disposition. Pour modifier l’alignement du texte, utilisez [**IDWriteTextLayout :: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
