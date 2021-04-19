---
description: Un segment de reconnaissance est l’unité d’encre de base qu’un module de reconnaissance utilise en interne pour produire un résultat de reconnaissance pour un objet d’encre particulier.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segments de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523417"
---
# <a name="recognition-segments"></a>Segments de reconnaissance

Un segment de reconnaissance est l’unité d’encre de base qu’un module de reconnaissance utilise en interne pour produire un résultat de reconnaissance pour un objet d’encre particulier. Un segment de reconnaissance est une collection de traits d’encre. Par exemple, un module de reconnaissance capable de reconnaître l’écriture manuscrite en anglais peut utiliser un mot comme segment de reconnaissance de base.

D’autres peuvent utiliser des parties de mots composites comme segments de base. Par exemple, en espagnol, les mots courts sont couramment combinés pour fournir des mots composites plus longs. « Damelo » est un mot espagnol qui est composé de trois mots « da me lo » (je le donne), mais il est écrit sous la forme d’un mot unique. Un module de reconnaissance espagnol peut reconnaître chaque sous-mot en tant que segment.

Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance. Étant donné que l’ambiguïté est impliquée dans la reconnaissance de l’entrée prévue de l’utilisateur, le module de reconnaissance peut retourner de nombreuses autres correspondances.

Pour plus d’informations sur les alternatives, consultez [alternatives](alternates.md).

 

 



