---
title: Reconnaissance de la palette
description: Votre application doit répondre aux messages WM \_ PALETTECHANGED, WM \_ QUERYNEWPALETTE et WM \_ Activate pour connaître et utiliser les palettes. Concevez votre application afin de sélectionner et de réaliser des palettes en réponse à ces messages.
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- OpenGL sur Windows, reconnaissance de la palette
- reconnaissance de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5172d3b0a353141900bd873d8f97d6a25ce570e54d180ce1c8b1ca949e51d8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936295"
---
# <a name="palette-awareness"></a>Reconnaissance de la palette

Votre application doit répondre aux messages [WM \_ PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)et [WM \_ Activate](../inputdev/wm-activate.md) pour connaître et utiliser les palettes. Concevez votre application afin de sélectionner et de réaliser des palettes en réponse à ces messages.

Pour plus d’informations sur les palettes et la reconnaissance des palettes, consultez les articles « reconnaissance des palettes » et « gestionnaire de palette : comment et pourquoi » sur le CD-ROM de la bibliothèque de développement Microsoft Developer Network.

 

 