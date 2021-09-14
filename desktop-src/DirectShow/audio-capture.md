---
description: Capture audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112165"
---
# <a name="audio-capture"></a>Capture audio

une application peut utiliser DirectShow pour capturer des données audio à partir de micros, de lecteurs de bandes et d’autres périphériques, par le biais des entrées de la carte son. Voici quelques exemples de scénarios courants :

-   Enregistrement d’une narration VoiceOver pour une copie ultérieure sur un flux vidéo.
-   Conversion de contenu audio analogue hérité en format numérique.
-   Capture de la voix ou de la musique pour la transmission sur un réseau.

Les utilisateurs finaux disposent de plusieurs options pour capturer l’audio de la carte son sur le disque dur. La plupart des cartes fournissent des applications pour le mixage et l’enregistrement à partir de leurs entrées audio. Windows fournit un magnétophone, une application utilitaire simple pour l’enregistrement à partir d’un microphone. le Windows media encoder peut être incorporé dans une application DirectShow sous la forme d’un [objet de média DirectX](directx-media-objects.md) (DMO). Cette section décrit comment intégrer la fonctionnalité de capture audio dans votre propre application à l’aide de DirectShow.

Cette section contient les rubriques suivantes :

-   [À propos du filtre de capture audio](about-the-audio-capture-filter.md)
-   [Sélection d’un périphérique de capture](selecting-a-capture-device.md)
-   [Création d’un Graph de capture audio](creating-an-audio-capture-graph.md)
-   [création d’un Graph de Capture Audio avec aperçu](creating-an-audio-capture-graph-with-preview.md)
-   [Définition des propriétés de capture audio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 



