---
description: Utilisez des contrôles Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les recommandations de Microsoft Active Accessibility. Cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Utilisation des contrôles Windows standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318290"
---
# <a name="using-standard-windows-controls"></a>Utilisation des contrôles Windows standard

Utilisez des contrôles Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les recommandations de Microsoft Active Accessibility. Cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).

Chaque contrôle Windows standard est une fenêtre distincte d’une classe spécifique. l’aide à l’accessibilité est donc notifiée lorsque le focus se déplace vers un nouveau contrôle. L’aide peut déterminer la classe de fenêtre de contrôles et tous les messages supplémentaires qu’elle peut envoyer pour interroger ou modifier l’état des contrôles. L’aide peut également identifier tous les contrôles enfants contenus dans une fenêtre parente et identifier le parent de n’importe quel contrôle.

Certains contrôles communs sont extrêmement flexibles et peuvent souvent remplacer des contrôles personnalisés moins accessibles et des contrôles owner-drawn. Par exemple, un affichage de liste peut remplacer une zone de liste owner-drawn pour afficher une case à cocher en regard de chaque élément. En guise d’autre exemple, le contrôle de bouton amélioré peut afficher à la fois des images et du texte. Auparavant, cela nécessitait l’utilisation d’un contrôle personnalisé.

 

 



