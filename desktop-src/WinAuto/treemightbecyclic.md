---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315281"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texte

L’arborescence est {0} Deep Levels. Cela peut indiquer que l’arborescence d’accessibilité est cyclique et qu’elle semble donc être infinie.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’arborescence des éléments est cyclique et la profondeur de l’arborescence peut être infinie.

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car il n’y aura aucune limite apparente au parcours des éléments dans l’application cible.

## <a name="possible-causes"></a>Causes possibles

Plusieurs éléments, ou leurs parents, sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation. Par exemple, la propriété d' [État](state-property.md) MSAA n’est pas mise à jour correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Instructions relatives à l’interaction avec l’expérience utilisateur Windows-clavier](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 