---
description: Demux le comportement de l’horloge
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Demux le comportement de l’horloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033495"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="39726-103">Demux le comportement de l’horloge</span><span class="sxs-lookup"><span data-stu-id="39726-103">Demux Clock Behavior</span></span>

<span data-ttu-id="39726-104">En mode push, le démultiplexeur MPEG-2 (demux) expose l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="39726-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="39726-105">Il agit comme une source dynamique, donc il est choisi comme horloge de référence graphique par défaut ; Pour plus d’informations, consultez la page [sources dynamiques](live-sources.md) .</span><span class="sxs-lookup"><span data-stu-id="39726-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="39726-106">Pour les flux de transport, demux synchronise son horloge avec le flux de données PCR qui correspond au flux audio ou vidéo le plus récemment mappé par l’application.</span><span class="sxs-lookup"><span data-stu-id="39726-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="39726-107">En interne, le demux suit les tables PAT et VPM.</span><span class="sxs-lookup"><span data-stu-id="39726-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="39726-108">Lorsque l’application mappe un PID de flux élémentaire à une broche de sortie, demux recherche le flux de la PCR pour ce PID et utilise ce flux de PCR.</span><span class="sxs-lookup"><span data-stu-id="39726-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="39726-109">(Actuellement, il n’existe aucun moyen pour l’application de spécifier directement le PID PCR.)</span><span class="sxs-lookup"><span data-stu-id="39726-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="39726-110">Pour les flux de programme, demux synchronise son horloge avec le flux de la SCR.</span><span class="sxs-lookup"><span data-stu-id="39726-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="39726-111">La synchronisation de l’horloge de filtre avec le flux PCR ou SCR empêche le dépassement de capacité négatif ou de dépassement de capacité des données, ce qui peut se produire si l’horloge du graphique varie de l’horloge du flux.</span><span class="sxs-lookup"><span data-stu-id="39726-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="39726-112">Le demux convertit également les valeurs de PTS PES en temps de référence DirectShow et utilise ces valeurs pour horodater les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="39726-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="39726-113">Les horodatages s’appliquent à la limite de cadre suivante ; Il n’y a aucune garantie que la limite de cadre s’aligne sur le début de l’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="39726-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="39726-114">Le demux garantit que les horodatages augmentent de manière monotone.</span><span class="sxs-lookup"><span data-stu-id="39726-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="39726-115">Cela signifie, par exemple, que si un flux de transport comprend un segment tel qu’un commercial qui a été créé avec une horloge différente de celle du programme principal, demux ajuste les horodatages de la présentation pour masquer la discontinuité des filtres en aval.</span><span class="sxs-lookup"><span data-stu-id="39726-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39726-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39726-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39726-117">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="39726-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



