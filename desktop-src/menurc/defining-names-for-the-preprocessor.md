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
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="f87be-103">Définition des noms pour le préprocesseur</span><span class="sxs-lookup"><span data-stu-id="f87be-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="f87be-104">Vous pouvez spécifier la compilation conditionnelle dans un script, selon qu’un nom est défini sur la ligne de commande RC avec l’option **/d** , ou dans le fichier ou un fichier include avec la directive [**\# define**](-define.md) .</span><span class="sxs-lookup"><span data-stu-id="f87be-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="f87be-105">Par exemple, supposons que votre application possède un menu contextuel qui doit apparaître uniquement avec les versions de débogage de l’application.</span><span class="sxs-lookup"><span data-stu-id="f87be-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="f87be-106">Quand vous compilez l’application pour une utilisation normale, le menu n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="f87be-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="f87be-107">L’exemple suivant montre les instructions qui peuvent être ajoutées au fichier de définition de ressource pour définir un menu Déboguer :</span><span class="sxs-lookup"><span data-stu-id="f87be-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

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

<span data-ttu-id="f87be-108">Lors de la compilation des ressources pour une version de débogage de l’application, vous pouvez inclure le menu Déboguer à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f87be-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="f87be-109">**RC-d déboguer MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="f87be-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="f87be-110">Pour compiler des ressources pour une version normale de l’application ? une qui n’inclut pas le menu Déboguer ? vous pouvez utiliser la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f87be-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="f87be-111">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="f87be-111">**rc myapp.rc**</span></span>

 

 




