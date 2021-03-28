---
description: Chaque analyse peut avoir sa propre profondeur de couleur.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Couleurs sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951560"
---
# <a name="colors-on-multiple-display-monitors"></a>Couleurs sur plusieurs moniteurs d’affichage

Chaque analyse peut avoir sa propre profondeur de couleur. Le système ajuste automatiquement les couleurs au fur et à mesure que les fenêtres passent par les moniteurs avec des profondeurs différentes. En général, cela produit de bons résultats. Toutefois, cela n’est pas toujours optimal. Pour tirer parti des fonctionnalités de couleur des différents moniteurs, consultez la section [peinture sur plusieurs écrans d’affichage](painting-on-multiple-display-monitors.md) qui suit.

Pour déterminer si toutes les analyses ont le même format de couleur, appelez [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le SM \_ SAMEDISPLAYFORMAT.

Si l’analyse principale est en palette, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) et [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) fonctionnent de la même manière qu’auparavant, mais sur toutes les analyses. En outre, les palettes de tous les appareils en palette sont synchronisées. Si le moniteur principal n’est pas en palette, **SelectPalette** et **RealizePalette** sélectionnent la palette dans l’arrière-plan et les appareils en palette ne sont pas synchronisés.

 

 
