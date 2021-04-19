---
description: Réglage de la télévision analogique
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Réglage de la télévision analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514728"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="75232-103">Réglage de la télévision analogique</span><span class="sxs-lookup"><span data-stu-id="75232-103">Analog Television Tuning</span></span>

<span data-ttu-id="75232-104">Le réglage est contrôlé par le filtre Tuner TV, via l’interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="75232-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="75232-105">L’interface IAMTVTuner hérite de IAMTuner.</span><span class="sxs-lookup"><span data-stu-id="75232-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="75232-106">Pour obtenir un pointeur vers l’interface, appelez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) comme suit :</span><span class="sxs-lookup"><span data-stu-id="75232-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="75232-107">Le premier paramètre indique d’effectuer une recherche dans le flux amont à partir du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="75232-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="75232-108">Tables de fréquence</span><span class="sxs-lookup"><span data-stu-id="75232-108">Frequency Tables</span></span>

<span data-ttu-id="75232-109">En interne, le filtre Tuner TV conserve une liste de tables de fréquence.</span><span class="sxs-lookup"><span data-stu-id="75232-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="75232-110">Chaque table de fréquence correspond aux fréquences de diffusion ou de câble pour un pays ou une région donné.</span><span class="sxs-lookup"><span data-stu-id="75232-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="75232-111">Il existe également une table de fréquence « Unicable » générique, qui est utilisée quand un pays ou une région n’a pas d’affectations de fréquence standard.</span><span class="sxs-lookup"><span data-stu-id="75232-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="75232-112">Chaque table de fréquence contient une liste de fréquences de paramétrage.</span><span class="sxs-lookup"><span data-stu-id="75232-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="75232-113">Pour certains pays ou régions, les index de la table correspondent directement aux numéros de canaux, en d’autres termes, la fréquence pour le canal n est la n ième entrée dans la table.</span><span class="sxs-lookup"><span data-stu-id="75232-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="75232-114">Pour certains pays ou régions, toutefois, il n’existe pas de correspondance directe entre les numéros de canaux et les fréquences.</span><span class="sxs-lookup"><span data-stu-id="75232-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="75232-115">Dans ce cas, l’application doit conserver une liste qui mappe les numéros de canaux (généralement choisis par l’utilisateur) aux entrées de la table de fréquence.</span><span class="sxs-lookup"><span data-stu-id="75232-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="75232-116">Par exemple, ce que l’utilisateur voit comme « Channel 5 » peut être le numéro d’entrée 12 dans la table Frequency.</span><span class="sxs-lookup"><span data-stu-id="75232-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="75232-117">Pour plus d’informations, consultez réglage de la [TV analogique internationale](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="75232-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="75232-118">Opérations de paramétrage de base</span><span class="sxs-lookup"><span data-stu-id="75232-118">Basic Tuning Operations</span></span>

<span data-ttu-id="75232-119">Si le tuner prend en charge plusieurs modes de réception, tels que la radio TV et FM, appelez [**IAMTuner ::p \_ mode ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) pour sélectionner le mode.</span><span class="sxs-lookup"><span data-stu-id="75232-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="75232-120">La méthode [**IAMTuner :: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) retourne tous les modes que le tuner prend en charge.</span><span class="sxs-lookup"><span data-stu-id="75232-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="75232-121">Par exemple, le code suivant vérifie si le tuner prend en charge la radio FM et, le cas échéant, bascule vers ce mode.</span><span class="sxs-lookup"><span data-stu-id="75232-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="75232-122">Pour définir le pays ou la région, appelez la méthode [**IAMTuner ::p ut \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) .</span><span class="sxs-lookup"><span data-stu-id="75232-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="75232-123">Le tuner utilise cette valeur pour sélectionner la table de fréquence appropriée.</span><span class="sxs-lookup"><span data-stu-id="75232-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="75232-124">Pour plus d’informations, consultez [affectations de pays/région](country-region-assignments.md) .</span><span class="sxs-lookup"><span data-stu-id="75232-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="75232-125">Pour définir le canal, appelez la méthode de [**\_ canal IAMTuner ::p ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) .</span><span class="sxs-lookup"><span data-stu-id="75232-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="75232-126">L’argument de cette méthode n’est en fait pas un numéro de canal, mais plutôt un index dans la table de fréquence actuelle.</span><span class="sxs-lookup"><span data-stu-id="75232-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="75232-127">Comme décrit précédemment, le numéro d’index peut ou ne peut pas correspondre à un numéro de canal.</span><span class="sxs-lookup"><span data-stu-id="75232-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="75232-128">La méthode [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) renvoie les valeurs d’index minimale et maximale pour la table de fréquence actuelle.</span><span class="sxs-lookup"><span data-stu-id="75232-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="75232-129">Remplacement des entrées de fréquence</span><span class="sxs-lookup"><span data-stu-id="75232-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="75232-130">Il est possible que certaines entrées dans les tables de fréquence soient incorrectes ou deviennent obsolètes.</span><span class="sxs-lookup"><span data-stu-id="75232-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="75232-131">Par conséquent, un mécanisme est fourni pour remplacer des entrées individuelles à l’aide de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="75232-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="75232-132">Les spécificités sont expliquées dans la rubrique [réglage de TV analogique internationale](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="75232-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="75232-133">Chaque clé de Registre définit un « espace de paramétrage » qui contient une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="75232-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="75232-134">Chaque sous-clé remplace une entrée de fréquence.</span><span class="sxs-lookup"><span data-stu-id="75232-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="75232-135">Pour définir l’espace de réglage actuel, utilisez la méthode [**IAMTuner ::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) .</span><span class="sxs-lookup"><span data-stu-id="75232-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="75232-136">L’activation de l’espace de réglage remplace les entrées de fréquence dans la table de fréquence actuelle.</span><span class="sxs-lookup"><span data-stu-id="75232-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="75232-137">Par conséquent, il revient à l’application de maintenir une correspondance entre les espaces de réglage et les pays/régions.</span><span class="sxs-lookup"><span data-stu-id="75232-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="75232-138">La meilleure approche consiste simplement à utiliser l’identificateur de pays/région comme nom de l’espace de réglage.</span><span class="sxs-lookup"><span data-stu-id="75232-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="75232-139">Réglage précis des entrées de fréquence</span><span class="sxs-lookup"><span data-stu-id="75232-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="75232-140">Les fréquences de diffusion peuvent être ajustées ou réduites plusieurs kHz par la station de diffusion pour réduire les interférences potentielles avec les canaux voisins.</span><span class="sxs-lookup"><span data-stu-id="75232-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="75232-141">Compte tenu de la fréquence nominale, la carte tuner peut rechercher la fréquence exacte.</span><span class="sxs-lookup"><span data-stu-id="75232-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="75232-142">Le filtre Tuner TV dispose d’un mécanisme permettant d’enregistrer les fréquences ajustées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="75232-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="75232-143">Pour chaque entrée de la table Frequency, appelez la \_ méthode put Channel pour régler cette fréquence.</span><span class="sxs-lookup"><span data-stu-id="75232-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="75232-144">Le tuner recherche la fréquence la plus précise.</span><span class="sxs-lookup"><span data-stu-id="75232-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="75232-145">Vous pouvez vérifier si le tuner a atteint un verrou horizontal en appelant [**IAMTuner :: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span><span class="sxs-lookup"><span data-stu-id="75232-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="75232-146">Le filtre Tuner TV stocke également le résultat en interne.</span><span class="sxs-lookup"><span data-stu-id="75232-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="75232-147">Après avoir analysé toutes les fréquences, appelez la méthode [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) pour écrire les valeurs mises à jour dans le registre.</span><span class="sxs-lookup"><span data-stu-id="75232-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="75232-148">Les valeurs mises à jour sont stockées sous l’entrée de Registre pour l’espace de paramétrage actuel.</span><span class="sxs-lookup"><span data-stu-id="75232-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75232-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75232-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75232-150">Télévision analogique</span><span class="sxs-lookup"><span data-stu-id="75232-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



