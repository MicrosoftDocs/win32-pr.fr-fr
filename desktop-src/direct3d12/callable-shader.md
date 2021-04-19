---
description: Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque CallShader.
ms.assetid: ''
title: Nuanceur pouvant être appelé
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515557"
---
# <a name="callable-shader"></a><span data-ttu-id="021ce-103">Nuanceur pouvant être appelé</span><span class="sxs-lookup"><span data-stu-id="021ce-103">Callable Shader</span></span>

<span data-ttu-id="021ce-104">Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque [**CallShader**](callshader-function.md) .</span><span class="sxs-lookup"><span data-stu-id="021ce-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="021ce-105">Une structure de paramètre est fournie sur le site d’appel **CallShader** , qui doit correspondre à la structure de paramètre utilisée dans le nuanceur pouvant être appelé, pointée par l’index demandé dans la table de nuanceur pouvant être appelée fournie par la méthode [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="021ce-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="021ce-106">Le nuanceur pouvant être appelé doit déclarer ce paramètre comme *INOUT*.</span><span class="sxs-lookup"><span data-stu-id="021ce-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="021ce-107">En outre, le nuanceur pouvant être appelé peut lire les entrées de la dimension et de l’index de lancement.</span><span class="sxs-lookup"><span data-stu-id="021ce-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="021ce-108">Pour plus d’informations, consultez [**intrinsèques de valeurs système**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span><span class="sxs-lookup"><span data-stu-id="021ce-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="021ce-109">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="021ce-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="021ce-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="021ce-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




