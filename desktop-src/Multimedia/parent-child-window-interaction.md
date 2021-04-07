---
title: Interaction de la fenêtre Parent-Child
description: Interaction de la fenêtre Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725861"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="ea77c-103">Interaction de la fenêtre Parent-Child</span><span class="sxs-lookup"><span data-stu-id="ea77c-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="ea77c-104">Certains messages au niveau du système, tels que [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), sont envoyés uniquement aux fenêtres de niveau supérieur et avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="ea77c-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="ea77c-105">Si une fenêtre de capture est une fenêtre enfant, son parent doit transférer ces messages.</span><span class="sxs-lookup"><span data-stu-id="ea77c-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="ea77c-106">De même, si la fenêtre parente change de taille, il peut être nécessaire d’envoyer des messages de notification à la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="ea77c-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="ea77c-107">Inversement, si les dimensions de la vidéo capturée changent, la fenêtre de capture peut avoir besoin d’envoyer des messages de notification à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="ea77c-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="ea77c-108">La façon la plus simple de gérer cela consiste à toujours conserver les dimensions de la fenêtre de capture à la valeur de la taille du flux vidéo capturé, en avertissant le parent à chaque modification de ces dimensions.</span><span class="sxs-lookup"><span data-stu-id="ea77c-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea77c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea77c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea77c-110">Capturer des fenêtres</span><span class="sxs-lookup"><span data-stu-id="ea77c-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 