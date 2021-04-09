---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant son nom.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect :: GetParameterByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954002"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="8c2ed-103">ID3DXBaseEffect :: GetParameterByName, méthode</span><span class="sxs-lookup"><span data-stu-id="8c2ed-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="8c2ed-104">Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c2ed-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="8c2ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c2ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2ed-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c2ed-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2ed-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8c2ed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8c2ed-109">Handle du paramètre, ou **null** pour les paramètres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="8c2ed-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8c2ed-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c2ed-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c2ed-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2ed-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c2ed-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c2ed-113">Chaîne contenant le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2ed-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c2ed-114">Return value</span></span>

<span data-ttu-id="8c2ed-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8c2ed-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8c2ed-116">Retourne le handle du paramètre spécifié, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="8c2ed-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8c2ed-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2ed-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c2ed-118">Requirements</span></span>



| <span data-ttu-id="8c2ed-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c2ed-119">Requirement</span></span> | <span data-ttu-id="8c2ed-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c2ed-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2ed-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c2ed-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8c2ed-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2ed-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8c2ed-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c2ed-123">Library</span></span><br/> | <dl> <span data-ttu-id="8c2ed-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c2ed-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c2ed-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2ed-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8c2ed-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
