---
description: Vue d’ensemble du système DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Vue d’ensemble du système DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520588"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="ef03e-103">Vue d’ensemble du système DirectShow</span><span class="sxs-lookup"><span data-stu-id="ef03e-103">DirectShow System Overview</span></span>

<span data-ttu-id="ef03e-104">**Le défi des médias**</span><span class="sxs-lookup"><span data-stu-id="ef03e-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="ef03e-105">L’utilisation de multimédia présente plusieurs défis majeurs :</span><span class="sxs-lookup"><span data-stu-id="ef03e-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="ef03e-106">Les flux multimédias contiennent de grandes quantités de données, qui doivent être traitées très rapidement.</span><span class="sxs-lookup"><span data-stu-id="ef03e-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="ef03e-107">L’audio et la vidéo doivent être synchronisés afin qu’ils démarrent et s’arrêtent en même temps et qu’ils soient lus à la même vitesse.</span><span class="sxs-lookup"><span data-stu-id="ef03e-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="ef03e-108">Les données peuvent provenir de nombreuses sources, y compris des fichiers locaux, des réseaux informatiques, des émissions de télévision et des caméras vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef03e-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="ef03e-109">Les données sont disponibles dans différents formats, tels que Audio-Video entrelacé (AVI), le format ASF (Advanced Streaming Format), le MPEG (motion image experts Group) et la vidéo numérique (DV).</span><span class="sxs-lookup"><span data-stu-id="ef03e-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="ef03e-110">Le programmeur ne sait pas à l’avance quels périphériques matériels seront présents sur le système de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ef03e-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="ef03e-111">**La solution DirectShow**</span><span class="sxs-lookup"><span data-stu-id="ef03e-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="ef03e-112">DirectShow est conçu pour résoudre chacun de ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="ef03e-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="ef03e-113">Son principal objectif de conception est de simplifier la tâche de création d’applications multimédias numériques sur la plate-forme Windows, en isolant les applications de la complexité des transports de données, des différences matérielles et de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="ef03e-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="ef03e-114">Pour atteindre le débit nécessaire pour diffuser des données audio et vidéo, DirectShow utilise Direct3D et DirectSound chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="ef03e-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="ef03e-115">Ces technologies affichent les données efficacement sur le son et les cartes graphiques de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef03e-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="ef03e-116">DirectShow synchronise la lecture en encapsulant les données multimédias dans des échantillons horodatés.</span><span class="sxs-lookup"><span data-stu-id="ef03e-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="ef03e-117">Pour gérer la diversité des sources, formats et périphériques matériels possibles, DirectShow utilise une architecture modulaire dans laquelle l’application combine et met en correspondance différents composants logiciels appelés *filtres*.</span><span class="sxs-lookup"><span data-stu-id="ef03e-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="ef03e-118">DirectShow fournit des filtres qui prennent en charge la capture et le paramétrage des appareils basés sur le Windows Driver Model (WDM), ainsi que des filtres qui prennent en charge les cartes de capture Video for Windows (VfW) anciennes et les codecs écrits pour les interfaces ACM (audio compression Manager) et VCM (Video Compression Manager).</span><span class="sxs-lookup"><span data-stu-id="ef03e-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="ef03e-119">Le diagramme suivant illustre la relation entre une application, les composants DirectShow et certains composants matériels et logiciels pris en charge par DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ef03e-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![architecture de haut niveau](images/arch-oview2.png)

<span data-ttu-id="ef03e-121">Comme illustré ici, les filtres DirectShow communiquent avec, et contrôlent, un large éventail d’appareils, notamment le système de fichiers local, le tuner TV et les cartes de capture vidéo, les codecs VfW, l’affichage vidéo (par le biais de DirectDraw ou GDI) et la carte son (via DirectSound).</span><span class="sxs-lookup"><span data-stu-id="ef03e-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="ef03e-122">Par conséquent, DirectShow isole l’application des nombreuses complexités de ces appareils.</span><span class="sxs-lookup"><span data-stu-id="ef03e-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="ef03e-123">DirectShow fournit également des filtres de compression et de décompression natifs pour certains formats de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ef03e-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef03e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef03e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef03e-125">À propos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ef03e-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



