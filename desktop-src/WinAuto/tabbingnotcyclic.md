---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031463"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Texte

La tabulation dans cette application n’est pas cyclique. La tabulation vers l’avant ou vers {0} l’arrière ne revient pas au même contrôle.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Lors de l’utilisation de la navigation au clavier standard (Tab ou Maj + Tab), il n’est pas possible de parcourir l’arborescence d’éléments de la cible de vérification jusqu’à ce que l’élément de départ devienne l’élément de fin (en utilisant le même nombre de séquences de touches) en inversant la direction de traversée. Par exemple, la tabulation suivante (tabulation) x fois de l’élément A (0) à l’élément A (x), puis la tabulation vers l’arrière (Maj + Tab) x fois n’entraîne pas l’élément A (0) qui regagne le focus.

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car il n’existe pas de moyen prévisible de revenir à un contrôle après l’avoir visité.

## <a name="possible-causes"></a>Causes possibles

-   L’élément ou son parent est un contrôle personnalisé qui n’implémente pas correctement la tabulation. Par exemple, la propriété d’État MSAA n’est pas définie correctement.
-   Certaines applications, telles que le bloc-notes, présentent ce comportement de manière innateuse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 