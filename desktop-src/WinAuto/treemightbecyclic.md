---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614433"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texte

L’arborescence est {0} Deep Levels. Cela peut indiquer que l’arborescence d’accessibilité est cyclique et qu’elle semble donc être infinie.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

L’arborescence des éléments est cyclique et la profondeur de l’arborescence peut être infinie.

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car il n’y aura aucune limite apparente au parcours des éléments dans l’application cible.

## <a name="possible-causes"></a>Causes possibles

Plusieurs éléments, ou leurs parents, sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation. Par exemple, la propriété d' [État](state-property.md) MSAA n’est pas mise à jour correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Instructions relatives à l’interaction avec l’expérience utilisateur-clavier](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 