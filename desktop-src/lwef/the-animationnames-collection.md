---
title: Collection AnimationNames
description: Collection AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840053"
---
# <a name="the-animationnames-collection"></a>Collection AnimationNames

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La collection [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) est une collection spéciale qui contient la liste des noms d’animation compilés pour un caractère. Vous pouvez utiliser la collection pour énumérer les noms des animations d’un caractère. Par exemple, dans Visual Basic ou VBScript (2,0 ou version ultérieure), vous pouvez accéder à ces noms à l’aide de l’exemple **de code for each... Instructions suivantes** :


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Les éléments de la collection n’ont pas de propriétés, donc les éléments individuels ne sont pas accessibles directement.

Pour. Les caractères ACF, la collection retourne toutes les animations qui ont été définies pour le caractère, pas seulement celles qui ont été récupérées avec la méthode d' [**extraction**](get-method.md) .

 

 




