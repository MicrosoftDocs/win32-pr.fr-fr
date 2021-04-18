---
description: Retourne la taille du code d’octet du nuanceur, en octets.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: D3DXGetShaderSize, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522592"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="1fa1d-103">D3DXGetShaderSize fonction)</span><span class="sxs-lookup"><span data-stu-id="1fa1d-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="1fa1d-104">Retourne la taille du code d’octet du nuanceur, en octets.</span><span class="sxs-lookup"><span data-stu-id="1fa1d-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fa1d-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="1fa1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fa1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa1d-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fa1d-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa1d-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fa1d-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1fa1d-109">Pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="1fa1d-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa1d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fa1d-110">Return value</span></span>

<span data-ttu-id="1fa1d-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fa1d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fa1d-112">Retourne la taille du code d’octet du nuanceur, en octets.</span><span class="sxs-lookup"><span data-stu-id="1fa1d-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa1d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fa1d-113">Requirements</span></span>



| <span data-ttu-id="1fa1d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fa1d-114">Requirement</span></span> | <span data-ttu-id="1fa1d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa1d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa1d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fa1d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1fa1d-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa1d-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1fa1d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fa1d-118">Library</span></span><br/> | <dl> <span data-ttu-id="1fa1d-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fa1d-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1fa1d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa1d-121">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1fa1d-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
