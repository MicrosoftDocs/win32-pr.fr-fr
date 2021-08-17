---
description: Chaque fois qu’une application crée un contrôleur de domaine et commence immédiatement à appeler les fonctions de sortie ou de dessin GDI, il tire parti de l’espace de la page par défaut à l’espace de l’appareil et de l’espace de l’appareil aux transformations de la zone cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformations par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba34effd9d6d43ab3b0abc740250c58788a8ce2f1556e89c92b78af823e58c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469679"
---
# <a name="default-transformations"></a>Transformations par défaut

Chaque fois qu’une application crée un contrôleur de domaine et commence immédiatement à appeler les fonctions de sortie ou de dessin GDI, il tire parti de l’espace de la page par défaut à l’espace de l’appareil et de l’espace de l’appareil aux transformations de la zone cliente. Une transformation de l’espace entre les pages ne peut pas se produire tant que l’application n’appelle pas d’abord la fonction [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) pour définir le mode sur GM \_ Advanced, puis appelle la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

L’utilisation du \_ texte de mm (l’espace de page par défaut pour la transformation de l’espace de l’appareil) entraîne un mappage un-à-un ; autrement dit, un point donné dans l’espace de page est mappé au même point dans l’espace de l’appareil. Comme mentionné précédemment, cette transformation n’est pas spécifiée par une matrice. Au lieu de cela, il est obtenu en divisant la largeur de la fenêtre d’affichage par la largeur de la fenêtre et la hauteur de la fenêtre d’affichage par la hauteur de la fenêtre. Dans le cas par défaut, les dimensions de la fenêtre d’affichage sont de 1 pixel par 1 pixel et les dimensions de la fenêtre sont 1 unité de page par unité de page.

La transformation de l’espace périphérique au périphérique physique (zone client, bureau ou imprimante) produit toujours un mappage un-à-un. autrement dit, une unité de l’espace de l’appareil est toujours équivalente à une unité dans la zone cliente, sur le bureau ou sur une page. La traduction est le seul objectif de cette transformation. elle garantit que la sortie apparaît correctement dans la fenêtre d’une application, quel que soit l’endroit où cette fenêtre est déplacée sur le bureau.

L’aspect unique du texte de MM \_ est l’orientation de l’axe des y dans l’espace de page. Dans \_ le texte de mm, l’axe des y positif s’étend vers le bas et l’axe y négatif s’étend vers le haut.

 

 



