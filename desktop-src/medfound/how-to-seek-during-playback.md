---
description: Cette rubrique explique comment effectuer une recherche au cours de la lecture à l’aide de MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Comment rechercher pendant la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520405"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="31bd4-103">Comment rechercher pendant la lecture</span><span class="sxs-lookup"><span data-stu-id="31bd4-103">How to Seek During Playback</span></span>

<span data-ttu-id="31bd4-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="31bd4-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31bd4-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="31bd4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="31bd4-106">\]</span><span class="sxs-lookup"><span data-stu-id="31bd4-106">\]</span></span>

<span data-ttu-id="31bd4-107">Cette rubrique explique comment effectuer une recherche au cours de la lecture à l’aide de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="31bd4-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="31bd4-108">**Pour rechercher pendant la lecture**</span><span class="sxs-lookup"><span data-stu-id="31bd4-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="31bd4-109">Initialisez un **PROPVARIANT** pour contenir le temps de recherche en unités de 100 nanosecondes, sous la forme d’un **grand \_ entier** (**VT \_ i8**).</span><span class="sxs-lookup"><span data-stu-id="31bd4-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="31bd4-110">Appelez [**IMFPMediaPlayer :: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span><span class="sxs-lookup"><span data-stu-id="31bd4-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="31bd4-111">Spécifiez **MFP \_ POSITIONTYPE \_ 100 ns** pour le premier paramètre, puis transmettez le **PROPVARIANT** pour le deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="31bd4-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="31bd4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31bd4-112">Requirements</span></span>

<span data-ttu-id="31bd4-113">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31bd4-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31bd4-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31bd4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31bd4-115">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="31bd4-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



