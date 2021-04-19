---
description: À propos du contrôle du taux
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: À propos du contrôle du taux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515646"
---
# <a name="about-rate-control"></a><span data-ttu-id="20924-103">À propos du contrôle du taux</span><span class="sxs-lookup"><span data-stu-id="20924-103">About Rate Control</span></span>

<span data-ttu-id="20924-104">Dans Media Foundation, la *Vitesse* de lecture est exprimée sous la forme du rapport entre le taux de lecture actuel et le taux de lecture normal.</span><span class="sxs-lookup"><span data-stu-id="20924-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="20924-105">Par exemple, un taux de 2,0 est de deux fois la vitesse normale et 0,5 à une vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="20924-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="20924-106">Les valeurs négatives indiquent une lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="20924-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="20924-107">Un taux de lecture de-2,0 est lu en arrière dans le flux à deux reprises à la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="20924-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="20924-108">Un taux de zéro provoque le rendu d’une trame ; Après cela, l’horloge de la présentation n’avance pas.</span><span class="sxs-lookup"><span data-stu-id="20924-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="20924-109">Pour obtenir une autre image au taux de zéro, l’application doit rechercher une nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="20924-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="20924-110">Les applications utilisent les interfaces suivantes pour contrôler la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="20924-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="20924-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="20924-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="20924-112">Utilisé pour déterminer les taux de lecture les plus rapides et les plus lents possibles.</span><span class="sxs-lookup"><span data-stu-id="20924-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="20924-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="20924-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="20924-114">Utilisé pour modifier la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="20924-114">Used to change the playback rate.</span></span>

<span data-ttu-id="20924-115">Pour accéder à ces deux interfaces, appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="20924-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="20924-116">L’identificateur de service est le \_ service de contrôle de taux MF \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="20924-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="20924-117">En utilisant le service de contrôle de la fréquence, une application peut implémenter une lecture rapide et en avance rapide.</span><span class="sxs-lookup"><span data-stu-id="20924-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="20924-118">Éclaircir</span><span class="sxs-lookup"><span data-stu-id="20924-118">Thinning</span></span>

<span data-ttu-id="20924-119">La *réduction est un* processus qui réduit le nombre d’échantillons dans un flux, afin de réduire la vitesse de transmission globale.</span><span class="sxs-lookup"><span data-stu-id="20924-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="20924-120">Pour la vidéo, l’affinage s’effectue généralement en supprimant les images Delta et en ne livrant que les images clés.</span><span class="sxs-lookup"><span data-stu-id="20924-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="20924-121">Souvent, le pipeline peut prendre en charge des vitesses de lecture plus rapides à l’aide de la lecture fine, car la vitesse des données est inférieure, car les images delta ne sont pas décodées.</span><span class="sxs-lookup"><span data-stu-id="20924-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="20924-122">L’affinage ne modifie pas les horodatages ou les durées sur les échantillons.</span><span class="sxs-lookup"><span data-stu-id="20924-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="20924-123">Par exemple, si la vitesse nominale du flux vidéo est de 25 images par seconde, la durée de chaque image est toujours marquée comme 40 millisecondes, même si la source du média supprime toutes les images Delta.</span><span class="sxs-lookup"><span data-stu-id="20924-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="20924-124">Cela signifie qu’il y aura un intervalle de temps entre la fin d’une image et le début de la suivante.</span><span class="sxs-lookup"><span data-stu-id="20924-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="20924-125">Nettoyage</span><span class="sxs-lookup"><span data-stu-id="20924-125">Scrubbing</span></span>

<span data-ttu-id="20924-126">Le *nettoyage* est le processus qui consiste à rechercher instantanément des points spécifiques dans le flux en interagissant avec une barre de défilement, une chronologie ou une autre représentation visuelle du temps.</span><span class="sxs-lookup"><span data-stu-id="20924-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="20924-127">Le terme vient de l’ère des lecteurs de bandes ENROULES sur bande lorsqu’il s’agit de faire basculer une bande vers l’avant pour localiser une section, comme le nettoyage de la tête de lecture avec la bande.</span><span class="sxs-lookup"><span data-stu-id="20924-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="20924-128">Le nettoyage est implémenté dans Media Foundation en affectant à la vitesse de lecture la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="20924-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="20924-129">Pour plus d’informations, consultez [Comment effectuer un nettoyage](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="20924-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20924-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20924-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20924-131">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="20924-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="20924-132">Recherche, avance rapide et lecture inversée</span><span class="sxs-lookup"><span data-stu-id="20924-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="20924-133">Interfaces de service</span><span class="sxs-lookup"><span data-stu-id="20924-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



