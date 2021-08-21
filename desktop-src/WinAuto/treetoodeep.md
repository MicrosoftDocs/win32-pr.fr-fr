---
title: TreeTooDeep
description: TreeTooDeep
ms.assetid: 3FD4A1BE-4710-4A1F-9ED7-98D7FCBCD304
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201de20e9d1ccd34619cb711429d05fac15a507fc27a377211d5969a0a70b2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827584"
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

[Windows Instructions relatives à l’interaction avec l’expérience utilisateur-clavier](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 