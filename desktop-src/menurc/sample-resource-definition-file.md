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
# <a name="sample-resource-definition-file"></a><span data-ttu-id="2feea-103">Exemple de fichier de Resource-Definition</span><span class="sxs-lookup"><span data-stu-id="2feea-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="2feea-104">L’exemple suivant montre un fichier de script qui définit les ressources pour une application nommée Shapes :</span><span class="sxs-lookup"><span data-stu-id="2feea-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

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

<span data-ttu-id="2feea-105">L’instruction de [**curseur**](cursor-resource.md) nomme la ressource de curseur de l’application ShapesCursor et spécifie les formes de fichier de curseur. CUR, qui contient l’image de ce curseur.</span><span class="sxs-lookup"><span data-stu-id="2feea-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="2feea-106">L’instruction [**Icon**](icon-resource.md) nomme la ressource icône de l’application ShapesIcon et spécifie les formes de fichiers icône. ICO, qui contient l’image de cette icône.</span><span class="sxs-lookup"><span data-stu-id="2feea-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="2feea-107">L’instruction de [**menu**](menu-resource.md) définit un menu d’application nommé **ShapesMenu**, un menu contextuel avec cinq éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="2feea-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="2feea-108">Le corps de la définition de menu, entouré par des accolades, ou les mots clés **Begin** et **end** , spécifie chaque élément de menu et l’identificateur de menu qui est retourné lorsque l’utilisateur sélectionne cet élément.</span><span class="sxs-lookup"><span data-stu-id="2feea-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="2feea-109">Par exemple, le premier élément du menu, **Clear**, retourne l’ID d’identificateur de menu \_ Clear lorsque l’utilisateur le sélectionne.</span><span class="sxs-lookup"><span data-stu-id="2feea-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="2feea-110">Les identificateurs de menu sont définis dans le fichier d’en-tête de l’application, SHAPEs. H.</span><span class="sxs-lookup"><span data-stu-id="2feea-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




