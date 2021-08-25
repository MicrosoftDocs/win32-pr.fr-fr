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
ms.openlocfilehash: 1cbaf4e2263cd1978fe16d0fb1b4b96c6dfb6065986bb8648c124fec5b56b810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777269"
---
# <a name="pixels"></a>Pixels

Les fragments sont convertis en pixels dans le trame. Le trame est organisé en un ensemble de mémoires tampons logiques de la couleur, de la profondeur, du stencil et des mémoires tampons d’accumulation. La mémoire tampon de couleur elle-même se compose d’un avant gauche, du premier plan, du verso, de l’arrière-plan et d’un certain nombre de mémoires tampons auxiliaires. Vous pouvez émettre des fonctions pour contrôler ces mémoires tampons et les lire ou les copier directement à partir de celles-ci. (Notez que le contexte OpenGL particulier que vous utilisez peut ne pas fournir toutes ces mémoires tampons.)

-   [Opérations trame](framebuffer-operations.md)
-   [Lecture ou copie de pixels](reading-or-copying-pixels.md)
-   [Référence en pixels](pixels-reference.md)

 

 




