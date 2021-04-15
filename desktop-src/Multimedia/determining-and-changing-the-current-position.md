---
title: Détermination et modification de la position actuelle
description: Détermination et modification de la position actuelle
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart macro)
- MCIWndGetEnd macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462286"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="6343e-105">Détermination et modification de la position actuelle</span><span class="sxs-lookup"><span data-stu-id="6343e-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="6343e-106">Lorsqu’un fichier ou un appareil est associé à une fenêtre MCIWnd, la position de lecture est initialement définie au début du contenu, quel que soit le type de support.</span><span class="sxs-lookup"><span data-stu-id="6343e-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="6343e-107">Pendant la lecture, la position de lecture se déplace de manière linéaire dans le contenu et, si la lecture n’est pas interrompue, finit par atteindre la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="6343e-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="6343e-108">Si une interruption se produit, la position de lecture actuelle est l’emplacement auquel la lecture a été arrêtée ou suspendue.</span><span class="sxs-lookup"><span data-stu-id="6343e-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="6343e-109">Vous pouvez récupérer les emplacements pour le début et la fin du contenu à l’aide des macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) et [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="6343e-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="6343e-110">Vous pouvez déterminer la longueur du contenu en soustrayant la valeur retournée par **MCIWndGetStart** de la valeur retournée par **MCIWndGetEnd**, ou à l’aide de la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="6343e-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="6343e-111">Vous pouvez récupérer la position de lecture actuelle à l’aide de la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) , ou vous pouvez récupérer la position de lecture comme une chaîne se terminant par un caractère null à l’aide de la macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="6343e-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="6343e-112">Pour modifier la position de lecture actuelle, utilisez les macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)et [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="6343e-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="6343e-113">Vous pouvez déplacer la position de lecture au début du contenu à l’aide de **MCIWndHome** ou à la fin du contenu à l’aide de **MCIWndEnd**.</span><span class="sxs-lookup"><span data-stu-id="6343e-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="6343e-114">Utilisez **MCIWndSeek** pour déplacer la position de lecture vers n’importe quel emplacement du contenu.</span><span class="sxs-lookup"><span data-stu-id="6343e-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="6343e-115">Vous pouvez également parcourir le contenu à l’aide de la macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) .</span><span class="sxs-lookup"><span data-stu-id="6343e-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="6343e-116">À partir de la position de lecture actuelle, cette macro déplace la position de lecture vers l’avant ou vers l’arrière d’un incrément spécifié.</span><span class="sxs-lookup"><span data-stu-id="6343e-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="6343e-117">Les unités utilisées pour spécifier la position varient selon les différents types de médias et périphériques.</span><span class="sxs-lookup"><span data-stu-id="6343e-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="6343e-118">Par exemple, la position de lecture pour les fichiers AVI utilisés par l’appareil MCIAVI est mesurée en frames. la position de lecture pour les fichiers audio CD, Waveform-Audio et MIDI est mesurée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6343e-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="6343e-119">Les appareils pour d’autres types de supports et des appareils tiers peuvent utiliser d’autres unités.</span><span class="sxs-lookup"><span data-stu-id="6343e-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="6343e-120">Pour plus d’informations sur la détermination de ces unités, consultez [améliorations de la lecture](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="6343e-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




