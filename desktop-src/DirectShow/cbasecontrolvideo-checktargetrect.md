---
description: La méthode CheckTargetRect détermine si un rectangle cible est valide.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Méthode CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542554"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="ee661-103">Méthode CBaseControlVideo. CheckTargetRect</span><span class="sxs-lookup"><span data-stu-id="ee661-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="ee661-104">La `CheckTargetRect` méthode détermine si un rectangle cible est valide.</span><span class="sxs-lookup"><span data-stu-id="ee661-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee661-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee661-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="ee661-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee661-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="ee661-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="ee661-108">Pointeur vers le rectangle cible à vérifier.</span><span class="sxs-lookup"><span data-stu-id="ee661-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee661-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee661-109">Return value</span></span>

<span data-ttu-id="ee661-110">Retourne E \_ INVALIDARG s’il n’est pas valide ; sinon, retourne NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="ee661-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee661-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ee661-111">Remarks</span></span>

<span data-ttu-id="ee661-112">Cette fonction membre détermine si le rectangle cible demandé est valide.</span><span class="sxs-lookup"><span data-stu-id="ee661-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="ee661-113">Étant donné que le rectangle de destination spécifie une position dans le client logique de la fenêtre, les coordonnées peuvent être négatives, même si la largeur et la hauteur globales ne peuvent pas être égales à zéro ou à une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="ee661-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee661-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee661-114">Requirements</span></span>



| <span data-ttu-id="ee661-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee661-115">Requirement</span></span> | <span data-ttu-id="ee661-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee661-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee661-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee661-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee661-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee661-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee661-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee661-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee661-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ee661-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee661-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee661-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee661-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="ee661-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




