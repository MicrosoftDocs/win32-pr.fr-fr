---
title: Opérations trame
description: Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de traitement OpenGL, opérations trame
- framebuffers, opérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507122"
---
# <a name="framebuffer-operations"></a>Opérations trame

Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez [**glDrawBuffer**](gldrawbuffer.md). Vous utilisez quatre fonctions différentes pour masquer l’écriture de bits à chacun des framebuffers logiques une fois toutes les opérations par fragment effectuées :

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La fonction [**glAccum**](glaccum.md) contrôle l’opération de la mémoire tampon d’accumulation. Enfin, [**glClear**](glclear.md) définit chaque pixel dans un sous-ensemble spécifié des mémoires tampons sur la valeur spécifiée par [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).

 

 




