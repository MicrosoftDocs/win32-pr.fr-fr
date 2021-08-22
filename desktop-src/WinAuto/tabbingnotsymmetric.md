---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6bda8de3e07f0ac6be3aa3a2a7bd750508dead1f5c2662391a056b258b36d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644099"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Texte

La tabulation descendante et les transferts ne génèrent pas le même élément. ATTENDU, {0} mais reçu {1}

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Lors de l’utilisation de la navigation au clavier standard (Tab ou Maj + Tab), il n’est pas possible de répéter le chemin d’accès dans l’arborescence des éléments de la cible de vérification si la direction du parcours est inversée. Par exemple, la tabulation suivante (tabulation) x fois de l’élément A (0) à l’élément A (x), puis la tabulation vers l’arrière (Maj + Tab) x fois, l’élément A (0) regagne le focus via un ensemble différent d’éléments intermédiaires.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le parcours des éléments semble irrégulier et imprévisible.

## <a name="possible-causes"></a>Causes possibles

-   Plusieurs éléments ou leurs parents sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation. Par exemple, la propriété d’État MSAA n’est pas définie correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 