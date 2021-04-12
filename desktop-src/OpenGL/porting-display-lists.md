---
title: Portage des listes d’affichage
description: L’implémentation OpenGL des listes d’affichage est semblable à celle de l’application IRIS GL, avec deux exceptions dans OpenGL. vous ne pouvez pas modifier les listes d’affichage une fois que vous les avez créées et vous ne pouvez pas appeler de fonctions à partir des listes d’affichage.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Le portage du GL IRIS, afficher les listes
- Portage à partir de IRIS GL, afficher les listes
- portage vers OpenGL à partir de IRIS GL, afficher les listes
- Portage OpenGL depuis IRIS GL, afficher les listes
- afficher les listes, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309450"
---
# <a name="porting-display-lists"></a>Portage des listes d’affichage

L’implémentation OpenGL des listes d’affichage est semblable à l’implémentation IRIS GL, à deux exceptions près : dans OpenGL, vous ne pouvez pas modifier les listes d’affichage une fois que vous les avez créées et vous ne pouvez pas appeler de fonctions à partir des listes d’affichage.

Étant donné que vous ne pouvez pas modifier ou appeler des fonctions dans des listes d’affichage, ces fonctions IRIS GL n’ont pas d’équivalent dans OpenGL :

-   **editobj**
-   **objdelete**, **objinsert** et **objreplace**
-   **maketag**, **gentag**, **ISTAG** et **deltaG**
-   **callfunc**

Dans IRIS GL, vous utilisez les fonctions **makeobj** et **closeobj** pour créer des listes d’affichage. Dans OpenGL, vous utilisez [**glNewList**](glnewlist.md) et [**glEndList**](glendlist.md).

Le tableau suivant répertorie les fonctions IRIS GL Display List avec leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                                                      | Signification                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Crée une nouvelle liste d’affichage.                                   |
| **closeobj**     | **glEndList**                                                        | Signale la fin de la liste d’affichage.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Exécute une liste ou des listes d’affichage.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Teste l’existence de la liste d’affichage.                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Supprime un groupe contigu de listes d’affichage.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Génère le nombre donné de listes d’affichage vides contiguës. |



 

Cette rubrique contient des informations sur les éléments suivants.

-   [Portage de la fonction BBOX2](porting-the-bbox2-function.md)
-   [Portage des listes d’affichage modifiées](porting-edited-display-lists.md)
-   [Exemple de port d’une liste d’affichage](a-sample-port-of-a-display-list.md)

 

 




