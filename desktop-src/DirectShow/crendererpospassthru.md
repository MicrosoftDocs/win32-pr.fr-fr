---
description: La classe CRendererPosPassThru gère les commandes de recherche pour les filtres de convertisseur, en les passant en amont au filtre suivant.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: CRendererPosPassThru, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544432"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="5c0c0-103">CRendererPosPassThru, classe</span><span class="sxs-lookup"><span data-stu-id="5c0c0-103">CRendererPosPassThru class</span></span>

![hiérarchie de la classe crendererpospassthru](images/cutil14.png)

<span data-ttu-id="5c0c0-105">La `CRendererPosPassThru` classe gère les commandes de recherche pour les filtres de convertisseur, en les passant en amont au filtre suivant.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="5c0c0-106">Cette classe dérive de la classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="5c0c0-107">Elle ajoute la prise en charge de la mise en cache des horodatages à partir des exemples à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="5c0c0-108">Utilisez cette classe de la même façon que la classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="5c0c0-109">Pour plus d’informations, consultez la documentation de **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="5c0c0-110">Le filtre de convertisseur doit mettre à jour les `CRendererPosPassThru` horodatages mis en cache de l’objet, comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c0c0-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="5c0c0-111">Pour chaque exemple reçu par le filtre, appelez la méthode [**CRendererPosPassThru :: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="5c0c0-112">Lorsque le filtre est arrêté ou reçoit un appel **EndFlush** , appelez la méthode [**CRendererPosPassThru :: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="5c0c0-113">Lorsque le filtre reçoit une notification de fin de flux, appelez la méthode [**CRendererPosPassThru :: EOS**](crendererpospassthru-eos.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="5c0c0-114">Pour obtenir un exemple d’utilisation de cette classe, reportez-vous au code source [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="5c0c0-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="5c0c0-115">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="5c0c0-115">Public Methods</span></span>                                                            | <span data-ttu-id="5c0c0-116">Description</span><span class="sxs-lookup"><span data-stu-id="5c0c0-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="5c0c0-117">**CRendererPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="5c0c0-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="5c0c0-118">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="5c0c0-119">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="5c0c0-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="5c0c0-120">Récupère les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="5c0c0-121">**RegisterMediaTime**</span><span class="sxs-lookup"><span data-stu-id="5c0c0-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="5c0c0-122">Met en cache les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="5c0c0-123">**ResetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="5c0c0-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="5c0c0-124">Réinitialise les horodatages mis en cache à zéro.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="5c0c0-125">**EOS**</span><span class="sxs-lookup"><span data-stu-id="5c0c0-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="5c0c0-126">Met à jour les horodatages mis en cache après une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="5c0c0-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5c0c0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c0c0-127">Requirements</span></span>



| <span data-ttu-id="5c0c0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c0c0-128">Requirement</span></span> | <span data-ttu-id="5c0c0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c0c0-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0c0-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c0c0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5c0c0-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0c0-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c0c0-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5c0c0-132">Library</span></span><br/> | <dl> <span data-ttu-id="5c0c0-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0c0-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




