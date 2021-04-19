---
description: La méthode CopyPalette copie la palette de toute structure VIDEOINFO vers n’importe quelle structure VIDEOINFO en palette.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Méthode CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542733"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="c3a10-103">Méthode CImagePalette. CopyPalette</span><span class="sxs-lookup"><span data-stu-id="c3a10-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="c3a10-104">La `CopyPalette` méthode copie la palette de toute structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) vers toute structure en palette **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="c3a10-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3a10-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="c3a10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a10-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="c3a10-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a10-108">Pointeur vers le type de média source.</span><span class="sxs-lookup"><span data-stu-id="c3a10-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="c3a10-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a10-110">Pointeur vers le type de média de destination.</span><span class="sxs-lookup"><span data-stu-id="c3a10-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a10-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3a10-111">Return value</span></span>

<span data-ttu-id="c3a10-112">Retourne S \_ OK si la palette a été copiée.</span><span class="sxs-lookup"><span data-stu-id="c3a10-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="c3a10-113">Retourne \_ la valeur S false si le type de média source ou de destination n’a pas de palette.</span><span class="sxs-lookup"><span data-stu-id="c3a10-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a10-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c3a10-114">Remarks</span></span>

<span data-ttu-id="c3a10-115">Le type de média *pDEST* doit être un format en palette avec une profondeur de couleur de 8 bits ou moins.</span><span class="sxs-lookup"><span data-stu-id="c3a10-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="c3a10-116">Le type de média *pSrc* peut être n’importe quel type de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avec une palette, y compris les formats YUV et couleurs vraies avec des entrées de palette.</span><span class="sxs-lookup"><span data-stu-id="c3a10-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="c3a10-117">La méthode copie les entrées de palette de *pSrc* dans une nouvelle palette, puis attache la nouvelle palette à *pDEST*.</span><span class="sxs-lookup"><span data-stu-id="c3a10-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a10-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3a10-118">Requirements</span></span>



| <span data-ttu-id="c3a10-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3a10-119">Requirement</span></span> | <span data-ttu-id="c3a10-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3a10-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a10-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3a10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c3a10-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3a10-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3a10-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3a10-123">Library</span></span><br/> | <dl> <span data-ttu-id="c3a10-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3a10-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a10-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3a10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a10-126">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="c3a10-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




