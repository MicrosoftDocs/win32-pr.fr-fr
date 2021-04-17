---
title: À propos de la classe de fenêtre MCIWnd
description: À propos de la classe de fenêtre MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- MCIWnd (classe de fenêtre), à propos de
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379985"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="848b3-105">À propos de la classe de fenêtre MCIWnd</span><span class="sxs-lookup"><span data-stu-id="848b3-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="848b3-106">La classe de fenêtre MCIWnd est facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="848b3-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="848b3-107">En utilisant une seule fonction, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) votre application peut créer un contrôle qui joue sur tout appareil qui utilise l’interface de contrôle de média (MCI).</span><span class="sxs-lookup"><span data-stu-id="848b3-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="848b3-108">Ces appareils incluent les périphériques CD audio, Waveform-Audio, MIDI et vidéo.</span><span class="sxs-lookup"><span data-stu-id="848b3-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="848b3-109">L’automatisation de la lecture est également simple et rapide.</span><span class="sxs-lookup"><span data-stu-id="848b3-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="848b3-110">À l’aide d’une seule fonction et de deux macros, une application peut créer une fenêtre MCIWnd avec le périphérique multimédia approprié, lire l’appareil et fermer à la fois l’appareil et la fenêtre lorsque la lecture du contenu est terminée.</span><span class="sxs-lookup"><span data-stu-id="848b3-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="848b3-111">Certains appareils lisent du contenu stocké dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="848b3-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="848b3-112">D’autres périphériques, tels que les périphériques CD audio, lisent du contenu stocké sur un autre support.</span><span class="sxs-lookup"><span data-stu-id="848b3-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="848b3-113">À des fins de clarté, cette vue d’ensemble fait référence aux deux circonstances comme « lisant l’appareil ».</span><span class="sxs-lookup"><span data-stu-id="848b3-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




