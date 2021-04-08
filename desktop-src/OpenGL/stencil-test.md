---
title: Test de stencil
description: Le test de stencil ignore conditionnellement un fragment en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon du stencil et une valeur de référence.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Pipeline de traitement OpenGL, test stencil
- test stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675486"
---
# <a name="stencil-test"></a>Test de stencil

Le test de stencil ignore conditionnellement un fragment en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon du stencil et une valeur de référence. La fonction [**glStencilFunc**](glstencilfunc.md) spécifie la fonction de comparaison et la valeur de référence. Si le fragment réussit ou échoue au test du stencil, la valeur dans la mémoire tampon du stencil est modifiée en fonction des instructions spécifiées par [**glStencilOp**](glstencilop.md).

 

 




