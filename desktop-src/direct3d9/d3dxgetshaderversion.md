---
description: Retourne la version du nuanceur du nuanceur compilé.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: D3DXGetShaderVersion, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116222"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="99bc3-103">D3DXGetShaderVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="99bc3-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="99bc3-104">Retourne la version du nuanceur du nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="99bc3-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99bc3-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="99bc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99bc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bc3-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99bc3-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc3-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bc3-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99bc3-109">Pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="99bc3-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bc3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99bc3-110">Return value</span></span>

<span data-ttu-id="99bc3-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99bc3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99bc3-112">Retourne la version du nuanceur du nuanceur donné, ou zéro si la fonction de nuanceur est **null**.</span><span class="sxs-lookup"><span data-stu-id="99bc3-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bc3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99bc3-113">Requirements</span></span>



| <span data-ttu-id="99bc3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99bc3-114">Requirement</span></span> | <span data-ttu-id="99bc3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="99bc3-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99bc3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="99bc3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="99bc3-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="99bc3-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="99bc3-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99bc3-118">Library</span></span><br/> | <dl> <span data-ttu-id="99bc3-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99bc3-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="99bc3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99bc3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bc3-121">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="99bc3-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
