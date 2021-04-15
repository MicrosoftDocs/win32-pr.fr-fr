---
title: Test de la mémoire tampon de profondeur
description: Le test de mémoire tampon de profondeur ignore un fragment si une comparaison de profondeur échoue ; glDepthFunc spécifie la fonction de comparaison. Si le stencil est activé, le résultat de la comparaison de profondeur affecte également la valeur de mise à jour du tampon de stencil.
ms.assetid: 7c52b01d-399e-46fa-a16e-12bbd584f8ab
keywords:
- Pipeline de traitement OpenGL, test de mémoire tampon de profondeur
- test de la mémoire tampon de profondeur OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac837641af79f2c24a4f85cfa93ac0754226bea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380245"
---
# <a name="depth-buffer-test"></a><span data-ttu-id="31f4f-106">Test de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="31f4f-106">Depth-buffer Test</span></span>

<span data-ttu-id="31f4f-107">Le test de mémoire tampon de profondeur ignore un fragment si une comparaison de profondeur échoue ; [**glDepthFunc**](gldepthfunc.md) spécifie la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="31f4f-107">The depth-buffer test discards a fragment if a depth comparison fails; [**glDepthFunc**](gldepthfunc.md) specifies the comparison function.</span></span> <span data-ttu-id="31f4f-108">Si le stencil est activé, le résultat de la comparaison de profondeur affecte également la valeur de mise à jour du tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="31f4f-108">If stenciling is enabled, the result of the depth comparison also affects the stencil buffer update value.</span></span>

 

 




