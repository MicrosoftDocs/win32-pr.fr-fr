---
title: Définition des noms pour le préprocesseur
description: Vous pouvez spécifier la compilation conditionnelle dans un script, selon qu’un nom est défini sur la ligne de commande RC avec l’option/d, ou dans le fichier ou un fichier include avec la directive \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3bcf9c02b5a4da4487b0c82de8d8b0223662cb30f9529e82204fc66a3de91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972108"
---
# <a name="defining-names-for-the-preprocessor"></a>Définition des noms pour le préprocesseur

Vous pouvez spécifier la compilation conditionnelle dans un script, selon qu’un nom est défini sur la ligne de commande RC avec l’option **/d** , ou dans le fichier ou un fichier include avec la directive [**\# define**](-define.md) .

Par exemple, supposons que votre application possède un menu contextuel qui doit apparaître uniquement avec les versions de débogage de l’application. Quand vous compilez l’application pour une utilisation normale, le menu n’est pas inclus. L’exemple suivant montre les instructions qui peuvent être ajoutées au fichier de définition de ressource pour définir un menu Déboguer :

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

Lors de la compilation des ressources pour une version de débogage de l’application, vous pouvez inclure le menu Déboguer à l’aide de la commande suivante :

**RC-d déboguer MyApp. RC**

Pour compiler des ressources pour une version normale de l’application ? une qui n’inclut pas le menu Déboguer ? vous pouvez utiliser la commande suivante :

**RC MyApp. RC**

 

 




