---
title: Fonctions (test d’atteinte tactile)
description: Les rubriques de cette section fournissent les spécifications de référence pour les fonctions tactiles de test de positionnement.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106534936"
---
# <a name="touch-hit-testing-functions"></a>Fonctions de test de positionnement tactile

Les rubriques de cette section fournissent les spécifications de référence pour les [fonctions tactiles de test de positionnement](functions.md).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Retourne le score d’un polygone en tant que cible tactile probable (par rapport à tous les autres polygones qui croisent la zone de contact tactile) et un point tactile ajusté dans le polygone. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Retourne le score d’un rectangle en tant que cible tactile probable, par rapport à tous les autres rectangles qui croisent la zone de contact tactile et un point tactile ajusté dans le rectangle. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Retourne le score d’évaluation de proximité et les coordonnées de point tactile ajustées comme valeur compressée pour le rappel de [message WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) . <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Inscrit une fenêtre pour traiter l' [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Référence de test de positionnement tactile](touchhittest-reference.md)
