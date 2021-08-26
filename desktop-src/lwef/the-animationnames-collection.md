---
title: Collection AnimationNames
description: Collection AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c9ee781b836599ccf9689bfae974fd4cf3af32d75df2070e984ae9b6596f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960659"
---
# <a name="the-animationnames-collection"></a>Collection AnimationNames

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La collection [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) est une collection spéciale qui contient la liste des noms d’animation compilés pour un caractère. Vous pouvez utiliser la collection pour énumérer les noms des animations d’un caractère. par exemple, dans Visual Basic ou VBScript (2,0 ou version ultérieure), vous pouvez accéder à ces noms à l’aide de l’exemple **de code For Each... Instructions suivantes** :


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Les éléments de la collection n’ont pas de propriétés, donc les éléments individuels ne sont pas accessibles directement.

Pour. Les caractères ACF, la collection retourne toutes les animations qui ont été définies pour le caractère, pas seulement celles qui ont été récupérées avec la méthode d' [**extraction**](get-method.md) .

 

 




