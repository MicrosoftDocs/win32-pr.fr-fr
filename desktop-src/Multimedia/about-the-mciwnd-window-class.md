---
title: À propos de la classe de fenêtre MCIWnd
description: À propos de la classe de fenêtre MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- MCIWnd (classe de fenêtre), à propos de
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a75f9798c1bfe0ec4f67da0f990018143efd0285541b49a9035b9749a36de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065659"
---
# <a name="about-the-mciwnd-window-class"></a>À propos de la classe de fenêtre MCIWnd

La classe de fenêtre MCIWnd est facile à utiliser. En utilisant une seule fonction, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) votre application peut créer un contrôle qui joue sur tout appareil qui utilise l’interface de contrôle de média (MCI). Ces appareils incluent les périphériques CD audio, Waveform-Audio, MIDI et vidéo.

L’automatisation de la lecture est également simple et rapide. À l’aide d’une seule fonction et de deux macros, une application peut créer une fenêtre MCIWnd avec le périphérique multimédia approprié, lire l’appareil et fermer à la fois l’appareil et la fenêtre lorsque la lecture du contenu est terminée.

> [!Note]  
> Certains appareils lisent du contenu stocké dans des fichiers. D’autres périphériques, tels que les périphériques CD audio, lisent du contenu stocké sur un autre support. À des fins de clarté, cette vue d’ensemble fait référence aux deux circonstances comme « lisant l’appareil ».

 

 

 




