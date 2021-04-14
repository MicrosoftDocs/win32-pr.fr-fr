---
title: Pixels
description: Les fragments sont convertis en pixels dans le trame.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, pixels
- Pipeline de traitement OpenGL, pixels
- pixels OpenGL
- framebuffers, conversion de fragments en pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380366"
---
# <a name="pixels"></a>Pixels

Les fragments sont convertis en pixels dans le trame. Le trame est organisé en un ensemble de mémoires tampons logiques de la couleur, de la profondeur, du stencil et des mémoires tampons d’accumulation. La mémoire tampon de couleur elle-même se compose d’un avant gauche, du premier plan, du verso, de l’arrière-plan et d’un certain nombre de mémoires tampons auxiliaires. Vous pouvez émettre des fonctions pour contrôler ces mémoires tampons et les lire ou les copier directement à partir de celles-ci. (Notez que le contexte OpenGL particulier que vous utilisez peut ne pas fournir toutes ces mémoires tampons.)

-   [Opérations trame](framebuffer-operations.md)
-   [Lecture ou copie de pixels](reading-or-copying-pixels.md)
-   [Référence en pixels](pixels-reference.md)

 

 




