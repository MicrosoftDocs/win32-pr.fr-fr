---
description: Chaque analyse peut avoir sa propre profondeur de couleur.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Couleurs sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115319"
---
# <a name="colors-on-multiple-display-monitors"></a>Couleurs sur plusieurs moniteurs d’affichage

Chaque analyse peut avoir sa propre profondeur de couleur. Le système ajuste automatiquement les couleurs au fur et à mesure que les fenêtres passent par les moniteurs avec des profondeurs différentes. En général, cela produit de bons résultats. Toutefois, cela n’est pas toujours optimal. Pour tirer parti des fonctionnalités de couleur des différents moniteurs, consultez la section [peinture sur plusieurs écrans d’affichage](painting-on-multiple-display-monitors.md) qui suit.

Pour déterminer si toutes les analyses ont le même format de couleur, appelez [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le SM \_ SAMEDISPLAYFORMAT.

Si l’analyse principale est en palette, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) fonctionnent de la même manière qu’auparavant, mais sur toutes les analyses. En outre, les palettes de tous les appareils en palette sont synchronisées. Si le moniteur principal n’est pas en palette, **SelectPalette** et **RealizePalette** sélectionnent la palette dans l’arrière-plan et les appareils en palette ne sont pas synchronisés.

 

 
