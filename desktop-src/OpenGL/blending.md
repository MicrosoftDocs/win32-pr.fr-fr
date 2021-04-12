---
title: Fusion
description: La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de traitement OpenGL, fusion
- fusion de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310010"
---
# <a name="blending"></a><span data-ttu-id="c7db8-105">Fusion</span><span class="sxs-lookup"><span data-stu-id="c7db8-105">Blending</span></span>

<span data-ttu-id="c7db8-106">La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c7db8-106">Blending combines a fragment's R, G, B, and A values with those stored in the framebuffer at the corresponding location.</span></span> <span data-ttu-id="c7db8-107">La fusion, qui est exécutée uniquement en mode RVBA, dépend de la valeur alpha du fragment et de celle du pixel actuellement stocké correspondant ; elle peut également dépendre des valeurs RVB.</span><span class="sxs-lookup"><span data-stu-id="c7db8-107">The blending, which is performed only in RGBA mode, depends on the alpha value of the fragment and that of the corresponding currently stored pixel; it may also depend on the RGB values.</span></span> <span data-ttu-id="c7db8-108">Vous contrôlez la fusion avec [**glBlendFunc**](glblendfunc.md), avec lequel vous indiquez les facteurs de fusion source et de destination.</span><span class="sxs-lookup"><span data-stu-id="c7db8-108">You control blending with [**glBlendFunc**](glblendfunc.md), with which you indicate the source and destination blending factors.</span></span>

 

 




