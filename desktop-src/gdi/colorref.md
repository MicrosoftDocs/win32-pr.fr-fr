---
Description: La valeur COLORREF est utilisée pour spécifier une couleur RVB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (WINDEF. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996456"
---
# <a name="colorref"></a><span data-ttu-id="0d3ac-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="0d3ac-103">COLORREF</span></span>

<span data-ttu-id="0d3ac-104">La valeur COLORREF est utilisée pour spécifier une couleur [RVB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="0d3ac-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="0d3ac-105">Notes</span><span class="sxs-lookup"><span data-stu-id="0d3ac-105">Remarks</span></span>

<span data-ttu-id="0d3ac-106">Lorsque vous spécifiez une couleur [RVB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) explicite, la valeur **COLORREF** est au format hexadécimal suivant :</span><span class="sxs-lookup"><span data-stu-id="0d3ac-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="0d3ac-107">L’octet de poids faible contient une valeur pour l’intensité relative du rouge ; le deuxième octet contient une valeur pour le vert ; et le troisième octet contient une valeur pour le bleu.</span><span class="sxs-lookup"><span data-stu-id="0d3ac-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="0d3ac-108">L’octet de poids fort doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0d3ac-108">The high-order byte must be zero.</span></span> <span data-ttu-id="0d3ac-109">La valeur maximale d’un seul octet est 0xFF.</span><span class="sxs-lookup"><span data-stu-id="0d3ac-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="0d3ac-110">Pour créer une valeur de couleur **COLORREF** , utilisez la macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="0d3ac-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="0d3ac-111">Pour extraire les valeurs individuelles des composants rouge, vert et bleu d’une valeur de couleur, utilisez respectivement les macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)et [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .</span><span class="sxs-lookup"><span data-stu-id="0d3ac-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="0d3ac-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d3ac-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="0d3ac-113">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="0d3ac-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3ac-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0d3ac-114">Requirements</span></span>



| <span data-ttu-id="0d3ac-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d3ac-115">Requirement</span></span> | <span data-ttu-id="0d3ac-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d3ac-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3ac-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d3ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3ac-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d3ac-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0d3ac-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d3ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3ac-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d3ac-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d3ac-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d3ac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d3ac-122"><dt>WINDEF. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d3ac-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3ac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d3ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3ac-124">Vue d’ensemble des couleurs</span><span class="sxs-lookup"><span data-stu-id="0d3ac-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="0d3ac-125">Structures de couleurs</span><span class="sxs-lookup"><span data-stu-id="0d3ac-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="0d3ac-126">GetBValue</span><span class="sxs-lookup"><span data-stu-id="0d3ac-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="0d3ac-127">GetGValue</span><span class="sxs-lookup"><span data-stu-id="0d3ac-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="0d3ac-128">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="0d3ac-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="0d3ac-129">RGB</span><span class="sxs-lookup"><span data-stu-id="0d3ac-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




