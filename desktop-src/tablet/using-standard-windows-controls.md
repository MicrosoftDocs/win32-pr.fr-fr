---
description: utilisez des contrôles de Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les instructions de Active Accessibility Microsoft. cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: utilisation des contrôles de Windows Standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449272"
---
# <a name="using-standard-windows-controls"></a>utilisation des contrôles de Windows Standard

utilisez des contrôles de Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les instructions de Active Accessibility Microsoft. cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).

chaque contrôle de Windows standard est une fenêtre distincte d’une classe spécifique. l’aide à l’accessibilité est donc notifiée lorsque le focus se déplace vers un nouveau contrôle. L’aide peut déterminer la classe de fenêtre de contrôles et tous les messages supplémentaires qu’elle peut envoyer pour interroger ou modifier l’état des contrôles. L’aide peut également identifier tous les contrôles enfants contenus dans une fenêtre parente et identifier le parent de n’importe quel contrôle.

Certains contrôles communs sont extrêmement flexibles et peuvent souvent remplacer des contrôles personnalisés moins accessibles et des contrôles owner-drawn. Par exemple, un affichage de liste peut remplacer une zone de liste owner-drawn pour afficher une case à cocher en regard de chaque élément. En guise d’autre exemple, le contrôle de bouton amélioré peut afficher à la fois des images et du texte. Auparavant, cela nécessitait l’utilisation d’un contrôle personnalisé.

 

 



