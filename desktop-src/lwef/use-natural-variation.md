---
title: Utiliser la variation naturelle
description: Utiliser la variation naturelle
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6259730599966205f4751c4ada9b8ef361cedf6d1a1a59dd1ce7d67aaf0fb448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474507"
---
# <a name="use-natural-variation"></a>Utiliser la variation naturelle

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Bien que la cohérence de présentation dans l’interface conventionnelle de votre application, telle que les menus et les boîtes de dialogue, rend l’interface plus prévisible, fait varier l’animation et la sortie parlée dans l’interface du caractère. Le fait de faire varier les réponses du caractère de manière appropriée fournit une interface plus naturelle. Si un caractère adresse toujours l’utilisateur exactement de la même façon ; par exemple, en prononçant toujours les mêmes mots, l’utilisateur est susceptible de prendre en compte l’alésage de caractères, le désintérêt ou même le caractère impropre. La communication humaine implique rarement des répétitions précises. Même si vous répétez une opération dans une situation similaire, nous pouvons modifier le libellé, les gestes ou l’expression faciale.

Microsoft agent vous permet de créer des variantes d’un caractère. Lorsque vous définissez les animations d’un caractère, vous pouvez utiliser les probabilités de branchement sur n’importe quelle image d’animation pour modifier une animation quand elle est lue. Vous pouvez également assigner plusieurs animations à chaque État. Microsoft Agent choisit de façon aléatoire l’une des animations affectées chaque fois qu’il lance un État. Pour la sortie vocale, vous pouvez également inclure des barres verticales dans le texte de sortie pour faire varier automatiquement le texte prononcé. Par exemple, Microsoft Agent sélectionne aléatoirement l’une des instructions suivantes lors du traitement de ce texte dans le cadre de la méthode [**Speak**](speak-method.md) :

«Je peux affirmer cela. \| Je peux le prononcer. \| Je peux faire autre chose.»

 

 




