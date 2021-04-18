---
description: Transmet un \_ \_ \_ message de modification de la taille de la vidéo ce au gestionnaire de graphes de filtre.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Méthode CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532911"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="8c4d0-103">Méthode CBaseControlVideo. OnVideoSizeChange</span><span class="sxs-lookup"><span data-stu-id="8c4d0-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="8c4d0-104">Transmet un \_ \_ \_ message de modification de la taille de la vidéo ce au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c4d0-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="8c4d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c4d0-106">Parameters</span></span>

<span data-ttu-id="8c4d0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c4d0-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c4d0-108">Return value</span></span>

<span data-ttu-id="8c4d0-109">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="8c4d0-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8c4d0-110">Return code</span></span>                                                                                   | <span data-ttu-id="8c4d0-111">Description</span><span class="sxs-lookup"><span data-stu-id="8c4d0-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8c4d0-112"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8c4d0-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8c4d0-113">Échec.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="8c4d0-114"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8c4d0-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8c4d0-115">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c4d0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8c4d0-116">Remarks</span></span>

<span data-ttu-id="8c4d0-117">Un convertisseur vidéo doit appeler cette fonction membre chaque fois que la taille de la vidéo est modifiée ; elle est généralement appelée une fois après la connexion initiale.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="8c4d0-118">Si le convertisseur peut prendre en charge des modifications de format dynamiques (de 320 x 240 à 160 x 120), il doit également l’appeler après chaque modification.</span><span class="sxs-lookup"><span data-stu-id="8c4d0-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4d0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c4d0-119">Requirements</span></span>



| <span data-ttu-id="8c4d0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c4d0-120">Requirement</span></span> | <span data-ttu-id="8c4d0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c4d0-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4d0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c4d0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8c4d0-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c4d0-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c4d0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c4d0-124">Library</span></span><br/> | <dl> <span data-ttu-id="8c4d0-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c4d0-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4d0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c4d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4d0-127">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="8c4d0-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




