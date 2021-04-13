---
title: Utilisation d’objets pavage
description: Comme un polygone complexe est décrit et fractionné, il requiert des données associées, telles que les vertex, les bords et les fonctions de rappel.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilitaire OpenGL (GLU), pavage d’objets
- GLU (utilitaire OpenGL), pavage d’objets
- pavage d’objets OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309638"
---
# <a name="using-tessellation-objects"></a>Utilisation d’objets pavage

Comme un polygone complexe est décrit et fractionné, il requiert des données associées, telles que les vertex, les bords et les fonctions de rappel. Toutes ces données sont liées à un seul objet de pavage. Pour paver un polygone, vous utilisez d’abord la fonction [**gluNewTess**](glunewtess.md) qui crée un nouvel objet pavage et retourne un pointeur vers celui-ci. Un pointeur null est retourné si la fonction échoue.

Si vous n’avez plus besoin d’un objet polygonalisation, vous pouvez le supprimer et libérer toute la mémoire associée avec [**gluDeleteTess**](gludeletetess.md).

Vous pouvez réutiliser un seul objet pavage pour tous vos pavages. Cet objet est requis uniquement parce que les fonctions de bibliothèque peuvent avoir besoin d’effectuer leurs propres pavages, et qu’ils doivent pouvoir le faire sans interférer avec les facettes que votre programme exécute. Plusieurs objets de pavage sont également utiles si vous souhaitez utiliser différents jeux de rappels pour différents pavages. En général, toutefois, vous allouez un seul objet pavage et l’utilisez pour tous les pavages. Il n’y a pas vraiment besoin de le libérer, car il utilise une petite quantité de mémoire. En revanche, si vous écrivez une fonction de bibliothèque qui utilise le pavage GLU, veillez à libérer tous les objets de pavage que vous créez.

 

 




