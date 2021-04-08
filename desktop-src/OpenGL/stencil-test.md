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
# <a name="stencil-test"></a><span data-ttu-id="f7054-105">Test de stencil</span><span class="sxs-lookup"><span data-stu-id="f7054-105">Stencil Test</span></span>

<span data-ttu-id="f7054-106">Le test de stencil ignore conditionnellement un fragment en fonction du résultat d’une comparaison entre la valeur dans la mémoire tampon du stencil et une valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="f7054-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="f7054-107">La fonction [**glStencilFunc**](glstencilfunc.md) spécifie la fonction de comparaison et la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="f7054-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="f7054-108">Si le fragment réussit ou échoue au test du stencil, la valeur dans la mémoire tampon du stencil est modifiée en fonction des instructions spécifiées par [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="f7054-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




