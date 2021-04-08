---
description: Active ou désactive les optimisations de l’UC.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: D3DXCpuOptimizations, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762200"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="777a9-103">D3DXCpuOptimizations fonction)</span><span class="sxs-lookup"><span data-stu-id="777a9-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="777a9-104">Active ou désactive les optimisations de l’UC.</span><span class="sxs-lookup"><span data-stu-id="777a9-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="777a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="777a9-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="777a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="777a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777a9-107">*Activer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="777a9-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="777a9-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="777a9-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="777a9-109">**True** pour activer les optimisations de l’UC ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="777a9-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777a9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="777a9-110">Return value</span></span>

<span data-ttu-id="777a9-111">Type : optimisation de l' **[ **\_ UC \_ D3DX**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="777a9-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="777a9-112">Retourne le type d’UC détecté et pour lequel des optimisations existent (consultez [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).</span><span class="sxs-lookup"><span data-stu-id="777a9-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="777a9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="777a9-113">Requirements</span></span>



| <span data-ttu-id="777a9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="777a9-114">Requirement</span></span> | <span data-ttu-id="777a9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="777a9-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="777a9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="777a9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="777a9-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="777a9-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="777a9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="777a9-118">Library</span></span><br/> | <dl> <span data-ttu-id="777a9-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="777a9-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="777a9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="777a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="777a9-121">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="777a9-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
