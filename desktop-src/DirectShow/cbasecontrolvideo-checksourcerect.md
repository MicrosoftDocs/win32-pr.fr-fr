---
description: Détermine si un rectangle source est valide.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Méthode CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537978"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="f2b59-103">Méthode CBaseControlVideo. CheckSourceRect</span><span class="sxs-lookup"><span data-stu-id="f2b59-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="f2b59-104">Détermine si un rectangle source est valide.</span><span class="sxs-lookup"><span data-stu-id="f2b59-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2b59-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="f2b59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2b59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b59-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f2b59-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f2b59-108">Pointeur vers le rectangle source à vérifier.</span><span class="sxs-lookup"><span data-stu-id="f2b59-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b59-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2b59-109">Return value</span></span>

<span data-ttu-id="f2b59-110">Retourne E \_ INVALIDARG s’il n’est pas valide ; sinon, retourne NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="f2b59-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b59-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f2b59-111">Remarks</span></span>

<span data-ttu-id="f2b59-112">Cette fonction membre vérifie que le rectangle source demandé ne dépasse pas la vidéo source disponible.</span><span class="sxs-lookup"><span data-stu-id="f2b59-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="f2b59-113">Les coordonnées gauche et supérieure ne peuvent pas être négatives, et la largeur et la hauteur ne peuvent pas dépasser la droite et la fin de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f2b59-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b59-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2b59-114">Requirements</span></span>



| <span data-ttu-id="f2b59-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2b59-115">Requirement</span></span> | <span data-ttu-id="f2b59-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b59-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b59-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2b59-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f2b59-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b59-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2b59-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2b59-119">Library</span></span><br/> | <dl> <span data-ttu-id="f2b59-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b59-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b59-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b59-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b59-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="f2b59-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




