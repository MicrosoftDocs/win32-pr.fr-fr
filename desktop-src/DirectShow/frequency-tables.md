---
description: Tables de fréquence
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tables de fréquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108542"
---
# <a name="frequency-tables"></a><span data-ttu-id="e541e-103">Tables de fréquence</span><span class="sxs-lookup"><span data-stu-id="e541e-103">Frequency Tables</span></span>

<span data-ttu-id="e541e-104">Le filtre Tuner TV (kstvtune.ax) dispose d’une liste interne de tables de fréquence.</span><span class="sxs-lookup"><span data-stu-id="e541e-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="e541e-105">Chaque table de fréquence contient une liste de fréquences et correspond aux fréquences de diffusion ou de câble pour un pays ou une région donné.</span><span class="sxs-lookup"><span data-stu-id="e541e-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="e541e-106">Une application s’adapte à une fréquence particulière en appelant la méthode de [**\_ canal IAMTuner ::p ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) avec l’index de la fréquence souhaitée.</span><span class="sxs-lookup"><span data-stu-id="e541e-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="e541e-107">Pour certains pays ou régions, les numéros d’index des tables de fréquence sont directement mappés aux numéros de canaux.</span><span class="sxs-lookup"><span data-stu-id="e541e-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="e541e-108">Toutefois, les numéros de canaux fixes ne conviennent pas à tous les marchés.</span><span class="sxs-lookup"><span data-stu-id="e541e-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="e541e-109">Par exemple, les numéros de canaux européens ne sont pas réellement utilisés par les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="e541e-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="e541e-110">Au lieu de cela, les consommateurs s’attendent à choisir et à attribuer leurs propres numéros de canaux pour les fréquences utilisées par les opérateurs de diffusion ou de câble dans leur région.</span><span class="sxs-lookup"><span data-stu-id="e541e-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="e541e-111">Pour ces pays/régions, les applications ne doivent pas exposer les numéros d’index directement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e541e-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="e541e-112">Instread, l’application doit conserver un mappage interne entre les numéros de canaux (présenté à l’utilisateur) et les index de fréquence (pour le paramétrage).</span><span class="sxs-lookup"><span data-stu-id="e541e-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="e541e-113">La plupart des opérateurs de câble non américains sont libres de diffuser sur les fréquences de leur choix, en mélangeant souvent des fréquences de différentes normes dans la même gamme de canaux.</span><span class="sxs-lookup"><span data-stu-id="e541e-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="e541e-114">Par conséquent, une table de fréquence « Unicable » est utilisée pour tout pays ou région qui ne dispose pas d’une autorité standard Cable Channel standards.</span><span class="sxs-lookup"><span data-stu-id="e541e-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="e541e-115">En outre, un mécanisme est fourni pour remplacer les fréquences individuelles dans les tables de fréquence.</span><span class="sxs-lookup"><span data-stu-id="e541e-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="e541e-116">Ce mécanisme est décrit dans la section suivante, [Overrides de fréquence](frequency-overrides.md).</span><span class="sxs-lookup"><span data-stu-id="e541e-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e541e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e541e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e541e-118">Réglage de la TV analogique internationale</span><span class="sxs-lookup"><span data-stu-id="e541e-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



