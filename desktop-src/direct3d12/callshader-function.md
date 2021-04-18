---
description: Appelle un autre nuanceur à partir d’un nuanceur.
ms.assetid: ''
title: Fonction CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519211"
---
# <a name="callshader-function"></a><span data-ttu-id="36c81-103">Fonction CallShader</span><span class="sxs-lookup"><span data-stu-id="36c81-103">CallShader function</span></span>

<span data-ttu-id="36c81-104">Appelle un autre nuanceur à partir d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="36c81-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36c81-105">Syntax</span></span>
<span data-ttu-id="36c81-106">Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :</span><span class="sxs-lookup"><span data-stu-id="36c81-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="36c81-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36c81-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="36c81-108">Entier non signé représentant l’index dans la table de [nuanceur pouvant être appelé](callable-shader.md) spécifiée dans l’appel à [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="36c81-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="36c81-109">Paramètres définis par l’utilisateur à passer au nuanceur pouvant être appelé.</span><span class="sxs-lookup"><span data-stu-id="36c81-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="36c81-110">Cette structure de paramètre doit correspondre à la structure de paramètre utilisée dans le nuanceur pouvant être appelé dans la table du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="36c81-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="36c81-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36c81-111">Return Value</span></span>

<span data-ttu-id="36c81-112">**void**</span><span class="sxs-lookup"><span data-stu-id="36c81-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="36c81-113">Notes</span><span class="sxs-lookup"><span data-stu-id="36c81-113">Remarks</span></span>

<span data-ttu-id="36c81-114">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="36c81-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="36c81-115">**Nuanceur pouvant être appelé**</span><span class="sxs-lookup"><span data-stu-id="36c81-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="36c81-116">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="36c81-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="36c81-117">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="36c81-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="36c81-118">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="36c81-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="36c81-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36c81-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c81-120">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="36c81-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




