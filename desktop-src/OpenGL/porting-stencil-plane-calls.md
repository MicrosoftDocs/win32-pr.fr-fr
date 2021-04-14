---
title: Portage des appels au plan du gabarit
description: Dans OpenGL, vous allouez des plans de stencil en demandant le format de pixel approprié avec le auxInitDisplayMode ou ChoosePixelFormat OpenGL.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Portage de l’IRIS dans le GL, plans de gabarit
- Portage à partir de IRIS GL, plans de stencil
- portage vers OpenGL à partir de IRIS GL, plans stencil
- Portage OpenGL à partir de IRIS GL, plans stencil
- plans de gabarit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310541"
---
# <a name="porting-stencil-plane-calls"></a>Portage des appels au plan du gabarit

Dans OpenGL, vous allouez des plans de stencil en demandant le format de pixel approprié avec le **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)OpenGL. Mission. Le tableau suivant répertorie les fonctions d’IRIS dans le GL qui affectent les plans de stencil et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL             | Fonction OpenGL                                         | Signification                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **stencil**( **true**,...) | [**glEnable**](glenable.md) (test de stencil du GL \_ \_ )      | Active les tests de stencil.                                 |
| **écrans**                  | [**glStencilOp**](glstencilop.md)                      | Définit des actions de test de stencil.                             |
| **gabarit**(... Func,...)  | [**glStencilFunc**](glstencilfunc.md)                  | Définit la fonction et la valeur de référence pour le test des stencils. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Spécifie les bits de stencil qui peuvent être écrits.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Spécifie la valeur Clear pour la mémoire tampon du stencil.      |
| **sclear**                   | [**glClear**](glclear.md) (bits de tampon de stencil du GL \_ \_ \_ ) |                                                        |



 

Les fonctions de comparaison de stencils et les opérations de réussite/échec de stencil sont presque équivalentes dans OpenGL et IRIS GL. Les indicateurs de fonction du gabarit IRIS GL-sont précédés de DF ; les indicateurs OpenGL avec GL. Les indicateurs d’opération de réussite/échec de l’IRIS GL sont précédés de ST ; les indicateurs OpenGL avec GL.

 

 




