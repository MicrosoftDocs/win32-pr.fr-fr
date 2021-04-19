---
description: La méthode ScaleSourceRect met à l’échelle un rectangle, s’il existe une différence entre la taille de la vidéo native et le format du type de média.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Méthode CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528019"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="49233-103">Méthode CDrawImage. ScaleSourceRect</span><span class="sxs-lookup"><span data-stu-id="49233-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="49233-104">La `ScaleSourceRect` méthode met à l’échelle un rectangle, s’il existe une différence entre la taille de la vidéo native et le format du type de média.</span><span class="sxs-lookup"><span data-stu-id="49233-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="49233-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49233-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="49233-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49233-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="49233-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="49233-108">Pointeur vers un rectangle non mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="49233-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49233-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49233-109">Return value</span></span>

<span data-ttu-id="49233-110">Retourne le rectangle mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="49233-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="49233-111">Notes</span><span class="sxs-lookup"><span data-stu-id="49233-111">Remarks</span></span>

<span data-ttu-id="49233-112">Dans la classe **CDrawImage** , cette méthode retourne *pSource* sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="49233-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="49233-113">Vous pouvez remplacer cette méthode si le filtre étire l’image vidéo entrante.</span><span class="sxs-lookup"><span data-stu-id="49233-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="49233-114">Par exemple, la taille de la vidéo Native peut être 320 240, mais le type de média sur la broche d’entrée peut être 640 480.</span><span class="sxs-lookup"><span data-stu-id="49233-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="49233-115">Dans ce cas, le filtre doit mettre à l’échelle le rectangle source d’un facteur de 2.</span><span class="sxs-lookup"><span data-stu-id="49233-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="49233-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49233-116">Requirements</span></span>



| <span data-ttu-id="49233-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49233-117">Requirement</span></span> | <span data-ttu-id="49233-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="49233-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49233-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="49233-119">Header</span></span><br/>  | <dl> <span data-ttu-id="49233-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49233-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49233-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49233-121">Library</span></span><br/> | <dl> <span data-ttu-id="49233-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49233-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49233-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49233-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49233-124">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="49233-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




