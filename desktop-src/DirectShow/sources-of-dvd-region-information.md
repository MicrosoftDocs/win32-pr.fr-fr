---
description: Sources d’informations sur les régions DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Sources d’informations sur les régions DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952417"
---
# <a name="sources-of-dvd-region-information"></a><span data-ttu-id="bc86f-103">Sources d’informations sur les régions DVD</span><span class="sxs-lookup"><span data-stu-id="bc86f-103">Sources of DVD Region Information</span></span>

<span data-ttu-id="bc86f-104">Il existe trois sources d’informations de région de DVD qui fonctionnent ensemble pour déterminer la région de lecture des DVD sur un PC Windows.</span><span class="sxs-lookup"><span data-stu-id="bc86f-104">There are three sources of DVD region information that work together to determine the region for DVD playback on a Windows PC.</span></span>

-   <span data-ttu-id="bc86f-105">Titre du DVD.</span><span class="sxs-lookup"><span data-stu-id="bc86f-105">DVD Title.</span></span> <span data-ttu-id="bc86f-106">La plupart des titres de DVD sont marqués pour une région spécifique.</span><span class="sxs-lookup"><span data-stu-id="bc86f-106">Most DVD titles are marked for a specific region.</span></span> <span data-ttu-id="bc86f-107">Certains titres peuvent être lus dans une seule région, certains peuvent être joués dans plusieurs régions, tandis que d’autres peuvent être joués dans toutes les régions.</span><span class="sxs-lookup"><span data-stu-id="bc86f-107">Some titles can be played in only one region, some can be played in multiple regions, and others can be played all regions.</span></span> <span data-ttu-id="bc86f-108">Les régions 1 à 6 ont été définies dans la spécification d’origine du DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="bc86f-108">Regions 1 through 6 were defined in the original DVD-Video specification.</span></span> <span data-ttu-id="bc86f-109">La région 7 n’est pas définie actuellement.</span><span class="sxs-lookup"><span data-stu-id="bc86f-109">Region 7 is currently undefined.</span></span> <span data-ttu-id="bc86f-110">La région 8 a été ajoutée dans 1999 pour des lieux spéciaux, tels que les avions.</span><span class="sxs-lookup"><span data-stu-id="bc86f-110">Region 8 was added in 1999 for special venues, such as airplanes.</span></span> <span data-ttu-id="bc86f-111">Les disques DVD-ROM (ceux sans zone vidéo) ne doivent pas contenir de code de région.</span><span class="sxs-lookup"><span data-stu-id="bc86f-111">DVD-ROM discs (those with no video zone) should not contain any region coding.</span></span>
-   <span data-ttu-id="bc86f-112">Lecteur de DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="bc86f-112">DVD-ROM Drive.</span></span> <span data-ttu-id="bc86f-113">Il existe deux types de lecteurs de DVD-ROM : les lecteurs RPC phase 1 (RPC1) et les lecteurs RPC phase 2 (RPC2).</span><span class="sxs-lookup"><span data-stu-id="bc86f-113">There are two types of DVD-ROM drives: RPC Phase 1 (RPC1) drives and RPC Phase 2 (RPC2) drives.</span></span> <span data-ttu-id="bc86f-114">Les lecteurs RPC1 n’ont pas de prise en charge matérielle intégrée pour la gestion des régions.</span><span class="sxs-lookup"><span data-stu-id="bc86f-114">RPC1 drives do not have built-in hardware support for region management.</span></span> <span data-ttu-id="bc86f-115">Pour ces lecteurs, Windows gère les informations sur le nombre de modifications de la région et la région ne peut être modifiée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="bc86f-115">For these drives, Windows maintains the region change count information and the region can be changed only once.</span></span> <span data-ttu-id="bc86f-116">Les lecteurs RPC2 maintiennent les informations sur le nombre de modifications de région dans le matériel et en général, la région de ces lecteurs peut être modifiée jusqu’à 5 fois.</span><span class="sxs-lookup"><span data-stu-id="bc86f-116">RPC2 drives maintain the region change count information in hardware and in general the region of such drives can be changed up to 5 times.</span></span>
-   <span data-ttu-id="bc86f-117">Décodeur DVD.</span><span class="sxs-lookup"><span data-stu-id="bc86f-117">DVD Decoder.</span></span> <span data-ttu-id="bc86f-118">Certains décodeurs DVD, matériel ou logiciel, sont définis pour une région spécifique.</span><span class="sxs-lookup"><span data-stu-id="bc86f-118">Some DVD decoders, hardware or software, are set for a specific region.</span></span> <span data-ttu-id="bc86f-119">En général, l’utilisateur ne peut pas modifier la région du décodeur.</span><span class="sxs-lookup"><span data-stu-id="bc86f-119">In general, the user cannot change the decoder's region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc86f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc86f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc86f-121">Prise en charge des modifications de région de DVD dans Windows</span><span class="sxs-lookup"><span data-stu-id="bc86f-121">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



