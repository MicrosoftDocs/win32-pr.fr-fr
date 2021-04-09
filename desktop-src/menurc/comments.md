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
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="6b290-105">Commentaires (menus et autres ressources)</span><span class="sxs-lookup"><span data-stu-id="6b290-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="6b290-106">RC prend en charge la syntaxe de style C pour les commentaires sur une seule ligne et les commentaires de bloc.</span><span class="sxs-lookup"><span data-stu-id="6b290-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="6b290-107">Les commentaires sur une seule ligne commencent par deux barres obliques (//) et s’exécutent jusqu’à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="6b290-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="6b290-108">L’exemple suivant illustre une instruction de ressource suivie d’un commentaire sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="6b290-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="6b290-109">Les commentaires de bloc commencent par un délimiteur ouvrant (/ \* ) et s’exécutent jusqu’à un délimiteur de fin ( \* /).</span><span class="sxs-lookup"><span data-stu-id="6b290-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="6b290-110">Les commentaires ne peuvent pas être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="6b290-110">Comments do not nest.</span></span> <span data-ttu-id="6b290-111">Voici un exemple de commentaire de bloc au début d’un fichier. rc.</span><span class="sxs-lookup"><span data-stu-id="6b290-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




