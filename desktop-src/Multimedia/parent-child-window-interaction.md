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
# <a name="parent-child-window-interaction"></a>Interaction de la fenêtre Parent-Child

Certains messages au niveau du système, tels que [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), sont envoyés uniquement aux fenêtres de niveau supérieur et avec chevauchement. Si une fenêtre de capture est une fenêtre enfant, son parent doit transférer ces messages.

De même, si la fenêtre parente change de taille, il peut être nécessaire d’envoyer des messages de notification à la fenêtre de capture. Inversement, si les dimensions de la vidéo capturée changent, la fenêtre de capture peut avoir besoin d’envoyer des messages de notification à la fenêtre parente. La façon la plus simple de gérer cela consiste à toujours conserver les dimensions de la fenêtre de capture à la valeur de la taille du flux vidéo capturé, en avertissant le parent à chaque modification de ces dimensions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capturer des fenêtres](capture-windows.md)
</dt> </dl>

 

 