---
description: Collecte d’informations de Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Collecte d’informations de Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514494"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="b7bba-103">Collecte d’informations de Fine-Tuning</span><span class="sxs-lookup"><span data-stu-id="b7bba-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="b7bba-104">Bien que les fréquences de câble soient généralement exactes, les fréquences de diffusion peuvent être ajustées ou réduites plusieurs kHz par la station de diffusion pour réduire les interférences potentielles avec les canaux voisins.</span><span class="sxs-lookup"><span data-stu-id="b7bba-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="b7bba-105">Lorsque le filtre Tuner TV est réglé sur un canal, il recherche le signal le plus précis.</span><span class="sxs-lookup"><span data-stu-id="b7bba-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="b7bba-106">Pour enregistrer ces informations dans le registre pour les opérations de paramétrage suivantes, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b7bba-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="b7bba-107">Appelez [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) pour déterminer la plage d’entrées de fréquence dans la table de fréquence actuelle.</span><span class="sxs-lookup"><span data-stu-id="b7bba-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="b7bba-108">Appelez la méthode [**IAMTuner ::p ut \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) une fois pour chaque index Frequency de la plage.</span><span class="sxs-lookup"><span data-stu-id="b7bba-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="b7bba-109">Appelez [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) pour enregistrer les informations de réglage précis dans le registre.</span><span class="sxs-lookup"><span data-stu-id="b7bba-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="b7bba-110">Les informations sont stockées sous la clé de Registre pour l’espace de réglage actuel.</span><span class="sxs-lookup"><span data-stu-id="b7bba-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="b7bba-111">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="b7bba-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="b7bba-112">Avec les versions antérieures du filtre Tuner TV, la méthode [**IAMTVTuner :: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) était recommandée pour le réglage précis.</span><span class="sxs-lookup"><span data-stu-id="b7bba-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="b7bba-113">Toutefois, cette méthode ignore toutes les substitutions de fréquence, donc son utilisation n’est plus recommandée.</span><span class="sxs-lookup"><span data-stu-id="b7bba-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="b7bba-114">Le code suivant est équivalent à la méthode **Autotune** , mais fonctionne correctement avec les remplacements de fréquence :</span><span class="sxs-lookup"><span data-stu-id="b7bba-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="b7bba-115">Avec la réception par diffusion, il n’est pas toujours possible d’obtenir un verrou horizontal, bien que l’image soit visible.</span><span class="sxs-lookup"><span data-stu-id="b7bba-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="b7bba-116">Dans ce cas, le matériel tuner aura un verrou de fréquence, mais le décodeur n’aura pas de verrou horizontal.</span><span class="sxs-lookup"><span data-stu-id="b7bba-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="b7bba-117">Cette condition peut être détectée lors de l’utilisation de l' [**instruction Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) ou [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) en examinant le code de retour.</span><span class="sxs-lookup"><span data-stu-id="b7bba-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="b7bba-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7bba-118">Value</span></span>    | <span data-ttu-id="b7bba-119">Description</span><span class="sxs-lookup"><span data-stu-id="b7bba-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bba-120">\_OK</span><span class="sxs-lookup"><span data-stu-id="b7bba-120">S\_OK</span></span>    | <span data-ttu-id="b7bba-121">L’opération de réglage a réussi et le tuner a obtenu un verrou de fréquence.</span><span class="sxs-lookup"><span data-stu-id="b7bba-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="b7bba-122">S \_ false</span><span class="sxs-lookup"><span data-stu-id="b7bba-122">S\_FALSE</span></span> | <span data-ttu-id="b7bba-123">Aucune erreur ne s’est produite pendant l’opération de réglage, mais le tuner n’a pas pu obtenir un verrou de fréquence.</span><span class="sxs-lookup"><span data-stu-id="b7bba-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="b7bba-124">Il est très improbable qu’il y ait un canal affichable résultant de cette opération.</span><span class="sxs-lookup"><span data-stu-id="b7bba-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="b7bba-125">Tout autre code de retour indique qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b7bba-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="b7bba-126">Une valeur de retour de S \_ OK ne garantit pas que le décodeur a un verrou horizontal.</span><span class="sxs-lookup"><span data-stu-id="b7bba-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="b7bba-127">La méthode [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) met à jour le paramètre *FoundSignal* pour indiquer si le verrou horizontal a été atteint ou non.</span><span class="sxs-lookup"><span data-stu-id="b7bba-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="b7bba-128">La méthode [**IAMTuner :: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) retourne les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="b7bba-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="b7bba-129">Toutefois, lorsque la valeur de retour est \_ OK, l’application a la possibilité d’ignorer le paramètre *FoundSignal* , car le tuner signale un verrou de fréquence.</span><span class="sxs-lookup"><span data-stu-id="b7bba-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="b7bba-130">Il existe une possibilité de verrou de fréquence sur le bruit, mais cette possibilité doit être pesée par rapport à la possibilité d’ignorer les canaux affichables.</span><span class="sxs-lookup"><span data-stu-id="b7bba-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="b7bba-131">Conversion du Registre</span><span class="sxs-lookup"><span data-stu-id="b7bba-131">Registry Conversion</span></span>

<span data-ttu-id="b7bba-132">Pour prendre en charge les remplacements de fréquence, le format interne de la clé de Registre qui contient des informations de réglage précis a changé.</span><span class="sxs-lookup"><span data-stu-id="b7bba-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="b7bba-133">Le format d’origine est toujours pris en charge pour la compatibilité descendante, mais il ne prend pas en charge les remplacements de fréquence.</span><span class="sxs-lookup"><span data-stu-id="b7bba-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="b7bba-134">L’ancien format de Registre est converti au nouveau format chaque fois que la méthode [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) est appelée.</span><span class="sxs-lookup"><span data-stu-id="b7bba-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="b7bba-135">Si votre application ajoute des remplacements de fréquence, elle doit appeler la méthode **StoreAutoTune** pour effectuer la conversion vers le nouveau format de registre.</span><span class="sxs-lookup"><span data-stu-id="b7bba-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="b7bba-136">Il n’est pas nécessaire de collecter des informations de réglage précis avant d’appeler **StoreAutoTune**.</span><span class="sxs-lookup"><span data-stu-id="b7bba-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7bba-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7bba-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7bba-138">Réglage de la TV analogique internationale</span><span class="sxs-lookup"><span data-stu-id="b7bba-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



