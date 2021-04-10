---
title: Définition des noms pour le préprocesseur
description: Vous pouvez spécifier la compilation conditionnelle dans un script, selon qu’un nom est défini sur la ligne de commande RC avec l’option/d, ou dans le fichier ou un fichier include avec la directive \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309426"
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

 

 




