---
description: L’exemple dans Brushes utilise des régions pour simuler une &\# 0034 ; avec zoom&\# 0034 ; affichage d’une bitmap monochrome de 8 par 8 pixels.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Utilisation de régions pour effectuer un test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558119"
---
# <a name="using-regions-to-perform-hit-testing"></a>Utilisation de régions pour effectuer un test de positionnement

L’exemple dans [Brushes](brushes.md) utilise des régions pour simuler une vue « zoomée » d’une bitmap monochrome de 8 par 8 pixels. En cliquant sur les pixels de cette image bitmap, l’utilisateur crée un pinceau personnalisé approprié pour les opérations de dessin. L’exemple montre comment utiliser la fonction [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) pour effectuer un test de positionnement et la fonction [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) pour inverser les couleurs dans une région.

 

 



