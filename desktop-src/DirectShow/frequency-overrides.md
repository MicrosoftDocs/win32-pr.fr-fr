---
description: Remplacements de fréquence
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Remplacements de fréquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520660"
---
# <a name="frequency-overrides"></a><span data-ttu-id="03ec3-103">Remplacements de fréquence</span><span class="sxs-lookup"><span data-stu-id="03ec3-103">Frequency Overrides</span></span>

<span data-ttu-id="03ec3-104">Un effort considérable a été passé pour s’assurer que les fréquences de diffusion et les affectations standard de couleur sont correctes pour chaque pays/région.</span><span class="sxs-lookup"><span data-stu-id="03ec3-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="03ec3-105">Même dans ce cas, il y a des situations où les tables de fréquence ne sont pas suffisantes, qui contiennent des erreurs ou qui deviennent obsolètes.</span><span class="sxs-lookup"><span data-stu-id="03ec3-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="03ec3-106">Pour résoudre ce problème, les fréquences listées dans les tables de fréquence du filtre Tuner TV peuvent être substituées sélectivement, à l’aide de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="03ec3-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="03ec3-107">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **TV System services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="03ec3-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="03ec3-108">À compter de Windows 7, la clé de Registre redirigée suivante est utilisée pour les applications x86 s’exécutant sur les versions x64 de Windows :</span><span class="sxs-lookup"><span data-stu-id="03ec3-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="03ec3-109">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="03ec3-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="03ec3-110">Les remplacements de fréquence sont regroupés dans des « espaces de paramétrage » définis par l’application, qui sont identifiés par un nombre.</span><span class="sxs-lookup"><span data-stu-id="03ec3-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="03ec3-111">L’exemple suivant montre un exemple de substitution :</span><span class="sxs-lookup"><span data-stu-id="03ec3-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="03ec3-112">Dans ce cas, « TS0-1 » indique l’espace de réglage 0 pour les fréquences de câble.</span><span class="sxs-lookup"><span data-stu-id="03ec3-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="03ec3-113">Le premier numéro identifie l’espace de réglage.</span><span class="sxs-lookup"><span data-stu-id="03ec3-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="03ec3-114">Le deuxième nombre est 0 pour les fréquences de diffusion ou 1 pour les fréquences de câble.</span><span class="sxs-lookup"><span data-stu-id="03ec3-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="03ec3-115">La sous-clé nommée « 12 » remplace la valeur de fréquence pour la fréquence à l’index 12 dans la table de fréquence actuelle.</span><span class="sxs-lookup"><span data-stu-id="03ec3-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="03ec3-116">La valeur de la sous-clé est une valeur **DWORD** qui spécifie la fréquence en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="03ec3-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="03ec3-117">Dans cet exemple, la fréquence est définie sur 67,25 MHz.</span><span class="sxs-lookup"><span data-stu-id="03ec3-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="03ec3-118">Les remplacements peuvent être définis pour tous les nombres de canaux compris entre 1 et 999 inclus.</span><span class="sxs-lookup"><span data-stu-id="03ec3-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="03ec3-119">Si le matériel de paramétrage ne prend pas en charge une fréquence donnée, la demande de réglage échoue.</span><span class="sxs-lookup"><span data-stu-id="03ec3-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="03ec3-120">Ce mécanisme peut également être utilisé pour créer des numéros de canaux en dehors de la plage existante dans la table Frequency.</span><span class="sxs-lookup"><span data-stu-id="03ec3-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="03ec3-121">La méthode [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retourne la plage de canaux étendue.</span><span class="sxs-lookup"><span data-stu-id="03ec3-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="03ec3-122">Par exemple, si la plage de canaux d’origine était comprise entre 1 et 158 et qu’une substitution de canal de « 200 » est ajoutée au registre, la méthode **ChannelMinMax** retourne 200 comme canal maximal.</span><span class="sxs-lookup"><span data-stu-id="03ec3-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="03ec3-123">Dans ce cas, les numéros de canaux de la plage comprise entre 159 et 199 n’ont aucune fréquence affectée. par conséquent, les demandes de paramétrage de cette plage échouent automatiquement.</span><span class="sxs-lookup"><span data-stu-id="03ec3-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="03ec3-124">La méthode [**IAMTuner ::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permet à l’application de choisir le jeu de remplacements et les informations de réglage précis à utiliser.</span><span class="sxs-lookup"><span data-stu-id="03ec3-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="03ec3-125">Les numéros d’espace de paramétrage sont arbitraires.</span><span class="sxs-lookup"><span data-stu-id="03ec3-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="03ec3-126">L’application est responsable de la gestion de la relation entre l’espace de réglage et la table de fréquence.</span><span class="sxs-lookup"><span data-stu-id="03ec3-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="03ec3-127">L’approche la plus simple consiste à utiliser le code de pays/région comme nombre d’espaces de réglage.</span><span class="sxs-lookup"><span data-stu-id="03ec3-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="03ec3-128">Ensuite, chaque fois que l’application bascule vers un nouveau code de pays/région, elle bascule également vers le même espace de paramétrage (dans cet ordre).</span><span class="sxs-lookup"><span data-stu-id="03ec3-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03ec3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03ec3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ec3-130">Réglage de la TV analogique internationale</span><span class="sxs-lookup"><span data-stu-id="03ec3-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



