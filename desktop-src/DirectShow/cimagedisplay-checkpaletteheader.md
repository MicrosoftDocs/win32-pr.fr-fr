---
description: La méthode CheckPaletteHeader valide les entrées de palette dans une structure VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Méthode CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542711"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="04b9b-103">Méthode CImageDisplay. CheckPaletteHeader</span><span class="sxs-lookup"><span data-stu-id="04b9b-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="04b9b-104">La `CheckPaletteHeader` méthode valide les entrées de palette dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="04b9b-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04b9b-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="04b9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04b9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b9b-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="04b9b-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="04b9b-108">Pointeur vers une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="04b9b-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b9b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04b9b-109">Return value</span></span>

<span data-ttu-id="04b9b-110">Retourne la **valeur true** si les entrées de palette sont valides, ou la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="04b9b-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b9b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="04b9b-111">Remarks</span></span>

<span data-ttu-id="04b9b-112">Si le format d’image n’est pas en palette, la méthode vérifie que **biClrUsed** est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="04b9b-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="04b9b-113">Dans le cas contraire, la méthode vérifie que l’indicateur de **bicompression** est bi \_ RGB ; **biClrImportant** n’est pas supérieur à **biClrUsed**; en raison de la profondeur de couleur, le nombre d’entrées de palette ne dépasse pas la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="04b9b-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b9b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04b9b-114">Requirements</span></span>



| <span data-ttu-id="04b9b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04b9b-115">Requirement</span></span> | <span data-ttu-id="04b9b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="04b9b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b9b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="04b9b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="04b9b-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04b9b-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04b9b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04b9b-119">Library</span></span><br/> | <dl> <span data-ttu-id="04b9b-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="04b9b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b9b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b9b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b9b-122">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="04b9b-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




