---
description: La méthode GetMediaPositionInterface récupère les pointeurs d’interface IMediaPosition et IMediaSeeking du filtre.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Méthode CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535885"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="d0981-103">Méthode CBaseRenderer. GetMediaPositionInterface</span><span class="sxs-lookup"><span data-stu-id="d0981-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="d0981-104">La `GetMediaPositionInterface` méthode récupère les pointeurs d’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du filtre.</span><span class="sxs-lookup"><span data-stu-id="d0981-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0981-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0981-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="d0981-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0981-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="d0981-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="d0981-108">Identificateur de référence de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d0981-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d0981-109">*ppv*</span><span class="sxs-lookup"><span data-stu-id="d0981-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="d0981-110">Adresse d’une variable qui reçoit le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="d0981-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0981-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0981-111">Return value</span></span>

<span data-ttu-id="d0981-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0981-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d0981-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0981-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d0981-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d0981-114">Return code</span></span>                                                                                   | <span data-ttu-id="d0981-115">Description</span><span class="sxs-lookup"><span data-stu-id="d0981-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="d0981-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0981-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0981-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d0981-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="d0981-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d0981-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0981-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d0981-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="d0981-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="d0981-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="d0981-121">Interface non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d0981-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0981-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d0981-122">Remarks</span></span>

<span data-ttu-id="d0981-123">Le filtre délègue toutes les commandes de recherche à un objet [**CRendererPosPassThru**](crendererpospassthru.md) , qui les transmet en amont.</span><span class="sxs-lookup"><span data-stu-id="d0981-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="d0981-124">Cette méthode crée l’objet **CRendererPosPassThru** , s’il n’existe pas encore, et le interroge pour l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="d0981-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="d0981-125">La variable membre [**CBaseRenderer :: m \_ pPosition**](cbaserenderer-m-pposition.md) stocke un pointeur vers l’objet **CRendererPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="d0981-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0981-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0981-126">Requirements</span></span>



| <span data-ttu-id="d0981-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0981-127">Requirement</span></span> | <span data-ttu-id="d0981-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0981-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0981-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0981-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d0981-130"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0981-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0981-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0981-131">Library</span></span><br/> | <dl> <span data-ttu-id="d0981-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0981-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0981-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0981-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0981-134">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="d0981-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




