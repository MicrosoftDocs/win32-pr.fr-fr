---
description: La méthode GetVideoSize récupère la largeur et la hauteur de la vidéo native.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Méthode CBaseControlVideo. GetVideoSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545636"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="06a9d-103">Méthode CBaseControlVideo. GetVideoSize</span><span class="sxs-lookup"><span data-stu-id="06a9d-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="06a9d-104">La `GetVideoSize` méthode récupère la largeur et la hauteur de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="06a9d-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06a9d-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="06a9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06a9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a9d-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="06a9d-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="06a9d-108">Pointeur vers la largeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="06a9d-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="06a9d-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="06a9d-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="06a9d-110">Pointeur désignant la hauteur de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="06a9d-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a9d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06a9d-111">Return value</span></span>

<span data-ttu-id="06a9d-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06a9d-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a9d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06a9d-113">Requirements</span></span>



| <span data-ttu-id="06a9d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06a9d-114">Requirement</span></span> | <span data-ttu-id="06a9d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a9d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a9d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="06a9d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="06a9d-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06a9d-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06a9d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06a9d-118">Library</span></span><br/> | <dl> <span data-ttu-id="06a9d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06a9d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a9d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06a9d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a9d-121">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="06a9d-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




