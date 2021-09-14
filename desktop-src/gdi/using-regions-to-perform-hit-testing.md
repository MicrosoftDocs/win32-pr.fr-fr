---
description: L’exemple dans Brushes utilise des régions pour simuler une &\# 0034 ; avec zoom&\# 0034 ; affichage d’une bitmap monochrome de 8 par 8 pixels.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Utilisation de régions pour effectuer un test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414312"
---
# <a name="using-regions-to-perform-hit-testing"></a>Utilisation de régions pour effectuer un test de positionnement

L’exemple dans [Brushes](brushes.md) utilise des régions pour simuler une vue « zoomée » d’une bitmap monochrome de 8 par 8 pixels. En cliquant sur les pixels de cette image bitmap, l’utilisateur crée un pinceau personnalisé approprié pour les opérations de dessin. L’exemple montre comment utiliser la fonction [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) pour effectuer un test de positionnement et la fonction [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) pour inverser les couleurs dans une région.

 

 



