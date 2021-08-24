---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052397"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Texte

La tabulation est passée à un élément en dehors du HWND cible.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

L’utilisation de la navigation au clavier standard (Tab ou Maj + Tab) entraîne le déplacement du focus en dehors du HWND de la cible de vérification.

AccChecker déplace l’arborescence d’éléments vers le HWND de niveau supérieur pour la cible de vérification choisie avant d’exécuter des tâches de vérification. Cela réduit le nombre d’erreurs fausses générées si un HWND choisi pour la vérification fait partie d’une zone client plus complexe.

## <a name="possible-causes"></a>Causes possibles

-   La cible de vérification n’a pas besoin d’une implémentation de tabulation pour fournir des fonctionnalités complètes.
-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.

 

 




