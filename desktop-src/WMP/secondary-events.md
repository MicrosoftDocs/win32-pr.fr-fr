---
title: Événements secondaires
description: Événements secondaires
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Lecteur Windows Media apparences, événements secondaires
- apparences, événements secondaires
- événements, secondaires
- écriture de code pour les apparences, événements secondaires
- événements secondaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fd121330a99c73ed7a52def712bb53949113745a8af0f4c01ded8f9aeaea4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735779"
---
# <a name="secondary-events"></a>Événements secondaires

Vous pouvez déterminer les autres événements qui se produisent lors du déclenchement d’un événement spécifique. Par exemple, quand l’utilisateur clique sur un bouton de la souris, vous pouvez être amené à savoir si la touche ALT a été déverrouillée en même temps.

## <a name="event-attributes"></a>Attributs d'événement

Les attributs d’événement suivants sont pris en charge pour les habillages :

-   **altKey**
-   **bouton**
-   **Une fois**
-   **client**
-   **ctrlKey**
-   **fromElement**
-   **offsetX**
-   **décalage**
-   **screenX**
-   **écran**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **keycode**

Pour plus d’informations sur ces attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Utilisation d’événements secondaires

vous pouvez uniquement traiter des attributs d’événement dans JScript code. Vous devez utiliser la syntaxe suivante :


```C++
event.eventattributename
```



*eventattributename* est le nom de l’attribut d’événement. par exemple, pour déterminer si la touche ALT a été enfoncée pendant un événement click, vous pouvez utiliser les lignes suivantes dans votre code JScript :


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements**](handling-events.md)
</dt> </dl>

 

 




