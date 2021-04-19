---
description: La méthode ShouldSkipFrame détermine si le filtre doit supprimer un échantillon spécifié.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Méthode CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528425"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="6adb5-103">Méthode CVideoTransformFilter. ShouldSkipFrame</span><span class="sxs-lookup"><span data-stu-id="6adb5-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="6adb5-104">La `ShouldSkipFrame` méthode détermine si le filtre doit supprimer un échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="6adb5-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="6adb5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6adb5-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="6adb5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6adb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6adb5-107">*Définis*</span><span class="sxs-lookup"><span data-stu-id="6adb5-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="6adb5-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6adb5-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6adb5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6adb5-109">Return value</span></span>

<span data-ttu-id="6adb5-110">Retourne la **valeur true** si le filtre doit supprimer cet exemple, ou **false** si le filtre doit traiter cet exemple.</span><span class="sxs-lookup"><span data-stu-id="6adb5-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="6adb5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6adb5-111">Remarks</span></span>

<span data-ttu-id="6adb5-112">Cette méthode retourne la **valeur true** si les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="6adb5-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="6adb5-113">L’exemple contient des horodatages.</span><span class="sxs-lookup"><span data-stu-id="6adb5-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="6adb5-114">Le temps de décodage moyen est d’au moins 25% de la durée de la trame.</span><span class="sxs-lookup"><span data-stu-id="6adb5-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="6adb5-115">Le convertisseur est actuellement au moins un frame en retard, comme indiqué par les messages de qualité.</span><span class="sxs-lookup"><span data-stu-id="6adb5-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="6adb5-116">Si vous ignorez l’image clé suivante, le frame n’arrivait pas plus d’une image tôt.</span><span class="sxs-lookup"><span data-stu-id="6adb5-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="6adb5-117">Dans le cadre de ce calcul, le filtre enregistre les informations suivantes lors du traitement des données :</span><span class="sxs-lookup"><span data-stu-id="6adb5-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="6adb5-118">Temps de décodage moyen au cours des 20 dernières trames (**m \_ itrAvgDecode**)</span><span class="sxs-lookup"><span data-stu-id="6adb5-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="6adb5-119">Nombre de trames depuis la dernière image clé (**m \_ nFramesSinceKeyFrame**)</span><span class="sxs-lookup"><span data-stu-id="6adb5-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="6adb5-120">Estimation du nombre de frames entre les images clés (**m \_ nKeyFramePeriod**)</span><span class="sxs-lookup"><span data-stu-id="6adb5-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="6adb5-121">Une fois que le filtre a supprimé un frame, il continue à déposer les images jusqu’à ce qu’il atteigne l’image clé suivante.</span><span class="sxs-lookup"><span data-stu-id="6adb5-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="6adb5-122">Si cette méthode retourne la **valeur true**, elle envoie également un événement de modification de la [**\_ \_ qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="6adb5-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="6adb5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6adb5-123">Requirements</span></span>



| <span data-ttu-id="6adb5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6adb5-124">Requirement</span></span> | <span data-ttu-id="6adb5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6adb5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6adb5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6adb5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6adb5-127"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6adb5-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6adb5-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6adb5-128">Library</span></span><br/> | <dl> <span data-ttu-id="6adb5-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6adb5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6adb5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6adb5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adb5-131">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6adb5-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




