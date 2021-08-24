---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3f168357cd67a7f22e81e985042a4983e7d8291bb6a0e2e343753959bcd6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828951"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Texte

Lors de la navigation en appelant {0} à partir du nœud testé, puis en appelant à plusieurs reprises {1} , nous avons terminé à l’enfant suivant : {2} . Cela ne correspondait pas au résultat de l’appel {3} sur le nœud testé, qui a produit : {4} . Au lieu de cela, l’enfant doit signaler comme son parent le nœud de test.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un problème est survenu lors de la navigation entre les enfants de l’élément. 1. Implémentation d’UI Automation incorrecte ou non valide.

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.

## <a name="possible-causes"></a>Causes possibles

Implémentation d’UI Automation incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




