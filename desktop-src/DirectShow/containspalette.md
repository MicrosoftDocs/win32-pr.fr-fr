---
description: La fonction ContainsPalette détermine si une structure VIDEOINFOHEADER spécifiée contient une palette.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: ContainsPalette, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526340"
---
# <a name="containspalette-function"></a><span data-ttu-id="17a9d-103">ContainsPalette fonction)</span><span class="sxs-lookup"><span data-stu-id="17a9d-103">ContainsPalette function</span></span>

<span data-ttu-id="17a9d-104">La fonction **ContainsPalette** détermine si une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) spécifiée contient une palette.</span><span class="sxs-lookup"><span data-stu-id="17a9d-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17a9d-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="17a9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17a9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a9d-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="17a9d-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="17a9d-108">Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="17a9d-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a9d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17a9d-109">Return value</span></span>

<span data-ttu-id="17a9d-110">Retourne la **valeur true** si bitdepth est inférieur ou égal à 8 (**bmiHeader. biBitCount**), ou si le nombre d’index de couleurs est supérieur à zéro (**bmiHeader. biClrUsed**).</span><span class="sxs-lookup"><span data-stu-id="17a9d-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="17a9d-111">Sinon, retourne **false** .</span><span class="sxs-lookup"><span data-stu-id="17a9d-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a9d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17a9d-112">Requirements</span></span>



| <span data-ttu-id="17a9d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17a9d-113">Requirement</span></span> | <span data-ttu-id="17a9d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="17a9d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a9d-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="17a9d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="17a9d-116"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17a9d-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="17a9d-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17a9d-117">Library</span></span><br/> | <dl> <span data-ttu-id="17a9d-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17a9d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a9d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17a9d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a9d-120">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="17a9d-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




