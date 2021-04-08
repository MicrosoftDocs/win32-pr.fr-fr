---
title: TreeTooDeep
description: TreeTooDeep
ms.assetid: 3FD4A1BE-4710-4A1F-9ED7-98D7FCBCD304
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681a929eca288584e9bd9ccd7b32920b10a72131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728532"
---
# <a name="treetoodeep"></a>TreeTooDeep

## <a name="text"></a>Texte

L’arborescence est {0} Deep Levels.

## <a name="type"></a>Type

Avertissement

## <a name="description"></a>Description

L’arborescence d’éléments peut être trop profonde.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le parcours des éléments semble prendre beaucoup de temps et peut apparaître cyclique.

## <a name="possible-causes"></a>Causes possibles

-   Plusieurs éléments ou leurs parents sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation. Par exemple, la propriété d’État MSAA n’est pas mise à jour correctement.
-   L’interface utilisateur de l’application est trop complexe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Instructions relatives à l’interaction avec l’expérience utilisateur Windows-clavier](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 