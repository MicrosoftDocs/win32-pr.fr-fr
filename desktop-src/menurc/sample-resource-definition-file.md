---
title: Exemple de fichier de Resource-Definition
description: Exemple de fichier de script qui définit les ressources pour une application nommée Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141258148b4e7a21d625a44b7f03d5e383c318d10447e050891f32b397c4283d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119225999"
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

 

 




