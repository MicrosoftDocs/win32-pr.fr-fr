---
title: Reconnaissance de la palette
description: Votre application doit répondre aux messages WM \_ PALETTECHANGED, WM \_ QUERYNEWPALETTE et WM \_ Activate pour connaître et utiliser les palettes. Concevez votre application afin de sélectionner et de réaliser des palettes en réponse à ces messages.
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- OpenGL sur Windows, reconnaissance de la palette
- reconnaissance de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ceab4c27f63c12977d072f84e789d1800b6557
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842674"
---
# <a name="palette-awareness"></a><span data-ttu-id="f3861-106">Reconnaissance de la palette</span><span class="sxs-lookup"><span data-stu-id="f3861-106">Palette Awareness</span></span>

<span data-ttu-id="f3861-107">Votre application doit répondre aux messages [WM \_ PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)et [WM \_ Activate](../inputdev/wm-activate.md) pour connaître et utiliser les palettes.</span><span class="sxs-lookup"><span data-stu-id="f3861-107">Your application must respond to the [WM\_PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM\_QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette), and [WM\_ACTIVATE](../inputdev/wm-activate.md) messages to be aware of and use palettes.</span></span> <span data-ttu-id="f3861-108">Concevez votre application afin de sélectionner et de réaliser des palettes en réponse à ces messages.</span><span class="sxs-lookup"><span data-stu-id="f3861-108">Design your application to select and realize palettes in response to these messages.</span></span>

<span data-ttu-id="f3861-109">Pour plus d’informations sur les palettes et la reconnaissance des palettes, consultez les articles « reconnaissance des palettes » et « gestionnaire de palette : comment et pourquoi » sur le CD-ROM de la bibliothèque de développement Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f3861-109">For more information on palettes and palette awareness, see the articles "Palette Awareness," and "The Palette Manager: How and Why" on the Microsoft Developer Network Development Library compact discs.</span></span>

 

 