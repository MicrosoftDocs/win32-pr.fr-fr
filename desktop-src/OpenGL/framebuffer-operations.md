---
title: Opérations trame
description: Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de traitement OpenGL, opérations trame
- framebuffers, opérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082329"
---
# <a name="framebuffer-operations"></a>Opérations trame

Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez [**glDrawBuffer**](gldrawbuffer.md). Vous utilisez quatre fonctions différentes pour masquer l’écriture de bits à chacun des framebuffers logiques une fois toutes les opérations par fragment effectuées :

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La fonction [**glAccum**](glaccum.md) contrôle l’opération de la mémoire tampon d’accumulation. Enfin, [**glClear**](glclear.md) définit chaque pixel dans un sous-ensemble spécifié des mémoires tampons sur la valeur spécifiée par [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).

 

 




