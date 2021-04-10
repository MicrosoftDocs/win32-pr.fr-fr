---
description: Obtient le handle d’une technique.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'ID3DXBaseEffect :: GetTechnique, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116290"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="ad43c-103">ID3DXBaseEffect :: GetTechnique, méthode</span><span class="sxs-lookup"><span data-stu-id="ad43c-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="ad43c-104">Obtient le handle d’une technique.</span><span class="sxs-lookup"><span data-stu-id="ad43c-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad43c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad43c-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ad43c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad43c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad43c-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad43c-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad43c-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad43c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad43c-109">Index technique.</span><span class="sxs-lookup"><span data-stu-id="ad43c-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad43c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad43c-110">Return value</span></span>

<span data-ttu-id="ad43c-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ad43c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ad43c-112">Retourne le handle de la technique spécifiée, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ad43c-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="ad43c-113">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ad43c-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad43c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad43c-114">Requirements</span></span>



| <span data-ttu-id="ad43c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad43c-115">Requirement</span></span> | <span data-ttu-id="ad43c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad43c-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad43c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad43c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ad43c-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad43c-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ad43c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad43c-119">Library</span></span><br/> | <dl> <span data-ttu-id="ad43c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad43c-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ad43c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad43c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad43c-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ad43c-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
