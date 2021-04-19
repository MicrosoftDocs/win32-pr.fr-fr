---
description: Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée.
ms.assetid: ''
title: Nuanceur manque
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514550"
---
# <a name="miss-shader"></a><span data-ttu-id="5bb5d-103">Nuanceur manque</span><span class="sxs-lookup"><span data-stu-id="5bb5d-103">Miss Shader</span></span>

<span data-ttu-id="5bb5d-104">Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="5bb5d-105">Cela est utile pour l’ombrage de l’arrière-plan ou du ciel.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="5bb5d-106">Le nuanceur d’échecs peut utiliser [**CallShader**](callshader-function.md) et **TraceRay** pour planifier davantage de travail.</span><span class="sxs-lookup"><span data-stu-id="5bb5d-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="5bb5d-107">Le nuanceur d’échecs doit inclure un paramètre de charge utile typée de structure définie par l’utilisateur correspondant à celui fourni à [**TraceRay**](traceray-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bb5d-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="5bb5d-108">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="5bb5d-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="5bb5d-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="5bb5d-109">Example</span></span>

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




