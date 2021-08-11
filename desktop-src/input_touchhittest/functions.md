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
ms.openlocfilehash: 83ab93fbff031423b6478926e499077ac78b1aec686d596ca069fda6d1b2298b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248356"
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
