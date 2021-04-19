---
description: La méthode CheckHeaderValidity valide une structure BITMAPINFOHEADER. Cette méthode est utile uniquement pour les types RVB non compressés, pas pour les types compressés ou les types YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Méthode CImageDisplay. CheckHeaderValidity (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537961"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="dc1ae-104">Méthode CImageDisplay. CheckHeaderValidity</span><span class="sxs-lookup"><span data-stu-id="dc1ae-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="dc1ae-105">La `CheckHeaderValidity` méthode valide une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="dc1ae-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="dc1ae-106">Cette méthode est utile uniquement pour les types RVB non compressés, pas pour les types compressés ou les types YUV.</span><span class="sxs-lookup"><span data-stu-id="dc1ae-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1ae-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc1ae-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="dc1ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc1ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1ae-109">*pInput*</span><span class="sxs-lookup"><span data-stu-id="dc1ae-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="dc1ae-110">Pointeur vers une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) contenant la structure **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="dc1ae-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1ae-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc1ae-111">Return value</span></span>

<span data-ttu-id="dc1ae-112">Retourne la **valeur true** si **BITMAPINFOHEADER** est valide, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dc1ae-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc1ae-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dc1ae-113">Remarks</span></span>

<span data-ttu-id="dc1ae-114">Cette méthode vérifie que les dimensions de l’image ne sont pas négatives ; le type de compression est BI \_ RGB ou \_ bits bi. les masques de couleur et de profondeur de couleur sont valides ; le membre **biplan** est égal à un et les membres **bisize** et **biSizeImage** sont corrects.</span><span class="sxs-lookup"><span data-stu-id="dc1ae-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="dc1ae-115">Il recherche également des erreurs courantes dans les entrées de palette, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="dc1ae-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc1ae-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc1ae-116">Requirements</span></span>



| <span data-ttu-id="dc1ae-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc1ae-117">Requirement</span></span> | <span data-ttu-id="dc1ae-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc1ae-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1ae-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc1ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dc1ae-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc1ae-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc1ae-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc1ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="dc1ae-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dc1ae-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1ae-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc1ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1ae-124">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="dc1ae-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




