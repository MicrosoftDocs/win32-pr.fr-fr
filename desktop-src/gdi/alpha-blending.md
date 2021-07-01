---
description: La fusion alpha est utilisée pour afficher une bitmap alpha, qui est une bitmap qui a des pixels transparents ou semi-transparents.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Fusion alpha (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4add2aca8ac4e2d7e1b24988eb5d40f80bac259c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120284"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="62c26-103">Fusion alpha (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="62c26-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="62c26-104">La *fusion alpha* est utilisée pour afficher une bitmap alpha, qui est une bitmap qui a des pixels transparents ou semi-transparents.</span><span class="sxs-lookup"><span data-stu-id="62c26-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="62c26-105">Outre un canal de couleur rouge, vert et bleu, chaque pixel d’une bitmap Alpha possède un composant de transparence appelé « *canal alpha*».</span><span class="sxs-lookup"><span data-stu-id="62c26-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="62c26-106">Le canal alpha contient généralement autant de bits qu’un canal de couleurs.</span><span class="sxs-lookup"><span data-stu-id="62c26-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="62c26-107">Par exemple, un canal alpha 8 bits peut représenter 256 niveaux de transparence, à partir de 0 (la bitmap entière est transparente) à 255 (la bitmap entière est opaque).</span><span class="sxs-lookup"><span data-stu-id="62c26-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="62c26-108">Les mécanismes de fusion alpha sont appelés en appelant [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), qui fait référence à la structure [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="62c26-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="62c26-109">Les valeurs alpha par pixel sont prises en charge uniquement pour la fonction RVB 32-BPP BI \_ .</span><span class="sxs-lookup"><span data-stu-id="62c26-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="62c26-110">Cette formule est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="62c26-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="62c26-111">Cela est représenté dans la mémoire, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="62c26-111">This is represented in memory as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="62c26-112">31:24</span><span class="sxs-lookup"><span data-stu-id="62c26-112">31:24</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-113">23:16</span><span class="sxs-lookup"><span data-stu-id="62c26-113">23:16</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-114">15:08</span><span class="sxs-lookup"><span data-stu-id="62c26-114">15:08</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-115">07:00</span><span class="sxs-lookup"><span data-stu-id="62c26-115">07:00</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="62c26-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="62c26-116">Alpha</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-117">Rouge</span><span class="sxs-lookup"><span data-stu-id="62c26-117">Red</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-118">Vert</span><span class="sxs-lookup"><span data-stu-id="62c26-118">Green</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="62c26-119">Bleu</span><span class="sxs-lookup"><span data-stu-id="62c26-119">Blue</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="62c26-120">Les bitmaps peuvent également être affichées avec un facteur de transparence appliqué à la bitmap entière.</span><span class="sxs-lookup"><span data-stu-id="62c26-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="62c26-121">Tout format bitmap peut être affiché avec une valeur alpha constante globale en définissant **SourceConstantAlpha** dans la structure [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="62c26-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="62c26-122">La valeur alpha constante globale a 256 niveaux de transparence, à partir de 0 (la totalité de la bitmap est complètement transparente) à 255 (la bitmap entière est entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="62c26-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="62c26-123">La valeur alpha constante globale est associée à la valeur alpha par pixel.</span><span class="sxs-lookup"><span data-stu-id="62c26-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="62c26-124">Pour obtenir un exemple, consultez [alpha blending a bitmap](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="62c26-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



