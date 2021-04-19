---
description: Lecture des flux audio karaoké
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Lecture des flux audio karaoké
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516347"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="99506-103">Lecture des flux audio karaoké</span><span class="sxs-lookup"><span data-stu-id="99506-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="99506-104">Le navigateur DVD peut lire DVD-Video disques avec des flux audio karaoké, mais la lecture karaoké requiert également un décodeur qui prend en charge le mixage de karaoké multicanal.</span><span class="sxs-lookup"><span data-stu-id="99506-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="99506-105">Plus précisément, le décodeur doit prendre en charge le [**jeu de propriétés Karaoké DVD**](dvd-karaoke-property-set.md) ( \_ propriété am \_ DVDKARAOKE).</span><span class="sxs-lookup"><span data-stu-id="99506-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="99506-106">Les disques de karaoké sont un type de DVD-Video disque et ont la même structure de navigation.</span><span class="sxs-lookup"><span data-stu-id="99506-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="99506-107">Les chansons sont généralement mises en forme en tant que titres, et les titres peuvent être regroupés en jeux de titres en fonction de l’intervenant, du style musical ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="99506-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="99506-108">La principale différence entre le karaoké et les autres types de DVD-Videos est le flux audio.</span><span class="sxs-lookup"><span data-stu-id="99506-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="99506-109">Les disques de karaoké contiennent tous un son multicanal, généralement Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="99506-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="99506-110">Les canaux 0 et 1 contiennent toujours la musique instrumentale d’arrière-plan, tandis que les canaux 2 à 5 peuvent contenir n’importe quelle combinaison de voix de guide, de Melodies de guide et d’effets sonores.</span><span class="sxs-lookup"><span data-stu-id="99506-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="99506-111">Une application karaoké peut contrôler le haut-parleur du volume et de la destination pour chaque canal auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="99506-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="99506-112">Lorsque le navigateur DVD détecte du contenu de karaoké sur un disque et passe en mode karaoké, il informe le décodeur, qui doit ensuite désactiver les trois canaux supérieurs (les canaux auxiliaires) jusqu’à ce qu’ils soient explicitement activés par une application.</span><span class="sxs-lookup"><span data-stu-id="99506-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="99506-113">Les tâches de base d’une application de karaoké sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="99506-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="99506-114">Déterminez le nombre de canaux auxiliaires et leur contenu à l’aide des méthodes [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .</span><span class="sxs-lookup"><span data-stu-id="99506-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="99506-115">Fournissez une interface utilisateur qui affiche le contenu du canal et permet aux utilisateurs d’activer ou de désactiver un canal auxiliaire à tout moment, à l’aide de [**IDvdControl2 :: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span><span class="sxs-lookup"><span data-stu-id="99506-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="99506-116">Ces étapes sont illustrées dans l’exemple d’application de DVD dans DVDCore. cpp, dans la méthode **GetAudioAttributes** .</span><span class="sxs-lookup"><span data-stu-id="99506-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99506-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99506-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99506-118">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="99506-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



