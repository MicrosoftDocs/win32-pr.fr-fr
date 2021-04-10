---
title: Exemple de fichier de Resource-Definition
description: Exemple de fichier de script qui définit les ressources pour une application nommée Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029551"
---
# <a name="sample-resource-definition-file"></a>Exemple de fichier de Resource-Definition

L’exemple suivant montre un fichier de script qui définit les ressources pour une application nommée Shapes :

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

L’instruction de [**curseur**](cursor-resource.md) nomme la ressource de curseur de l’application ShapesCursor et spécifie les formes de fichier de curseur. CUR, qui contient l’image de ce curseur.

L’instruction [**Icon**](icon-resource.md) nomme la ressource icône de l’application ShapesIcon et spécifie les formes de fichiers icône. ICO, qui contient l’image de cette icône.

L’instruction de [**menu**](menu-resource.md) définit un menu d’application nommé **ShapesMenu**, un menu contextuel avec cinq éléments de menu.

Le corps de la définition de menu, entouré par des accolades, ou les mots clés **Begin** et **end** , spécifie chaque élément de menu et l’identificateur de menu qui est retourné lorsque l’utilisateur sélectionne cet élément. Par exemple, le premier élément du menu, **Clear**, retourne l’ID d’identificateur de menu \_ Clear lorsque l’utilisateur le sélectionne. Les identificateurs de menu sont définis dans le fichier d’en-tête de l’application, SHAPEs. H.

 

 




