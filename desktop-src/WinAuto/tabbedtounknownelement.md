---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379789"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Texte

La tabulation est passée à un élément en dehors du HWND cible.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’utilisation de la navigation au clavier standard (Tab ou Maj + Tab) entraîne le déplacement du focus en dehors du HWND de la cible de vérification.

AccChecker déplace l’arborescence d’éléments vers le HWND de niveau supérieur pour la cible de vérification choisie avant d’exécuter des tâches de vérification. Cela réduit le nombre d’erreurs fausses générées si un HWND choisi pour la vérification fait partie d’une zone client plus complexe.

## <a name="possible-causes"></a>Causes possibles

-   La cible de vérification n’a pas besoin d’une implémentation de tabulation pour fournir des fonctionnalités complètes.
-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.

 

 




