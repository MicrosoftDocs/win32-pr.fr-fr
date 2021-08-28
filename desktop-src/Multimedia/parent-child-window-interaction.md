---
title: Interaction de la fenêtre Parent-Child
description: Interaction de la fenêtre Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b2ea050fda4cbc6ffc54e318a6a7d01e63db6ace0f1d71e3847f46b68b94ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136748"
---
# <a name="parent-child-window-interaction"></a>Interaction de la fenêtre Parent-Child

Certains messages au niveau du système, tels que [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), sont envoyés uniquement aux fenêtres de niveau supérieur et avec chevauchement. Si une fenêtre de capture est une fenêtre enfant, son parent doit transférer ces messages.

De même, si la fenêtre parente change de taille, il peut être nécessaire d’envoyer des messages de notification à la fenêtre de capture. Inversement, si les dimensions de la vidéo capturée changent, la fenêtre de capture peut avoir besoin d’envoyer des messages de notification à la fenêtre parente. La façon la plus simple de gérer cela consiste à toujours conserver les dimensions de la fenêtre de capture à la valeur de la taille du flux vidéo capturé, en avertissant le parent à chaque modification de ces dimensions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows de capture](capture-windows.md)
</dt> </dl>

 

 