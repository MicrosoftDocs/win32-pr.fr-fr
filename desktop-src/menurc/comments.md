---
title: Commentaires (menus et autres ressources)
description: RC prend en charge la syntaxe de style C pour les commentaires sur une seule ligne et les commentaires de bloc. Les commentaires sur une seule ligne commencent par deux barres obliques (//) et s’exécutent jusqu’à la fin de la ligne. L’exemple suivant illustre une instruction de ressource suivie d’un commentaire sur une seule ligne.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739628"
---
# <a name="comments-menus-and-other-resources"></a>Commentaires (menus et autres ressources)

RC prend en charge la syntaxe de style C pour les commentaires sur une seule ligne et les commentaires de bloc. Les commentaires sur une seule ligne commencent par deux barres obliques (//) et s’exécutent jusqu’à la fin de la ligne. L’exemple suivant illustre une instruction de ressource suivie d’un commentaire sur une seule ligne.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Les commentaires de bloc commencent par un délimiteur ouvrant (/ \* ) et s’exécutent jusqu’à un délimiteur de fin ( \* /). Les commentaires ne peuvent pas être imbriqués. Voici un exemple de commentaire de bloc au début d’un fichier. rc.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




