---
description: Obtient le handle d’une passe en recherchant son nom.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect :: GetPassByName, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524881"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="1d198-103">ID3DXBaseEffect :: GetPassByName, méthode</span><span class="sxs-lookup"><span data-stu-id="1d198-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="1d198-104">Obtient le handle d’une passe en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="1d198-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d198-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d198-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="1d198-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d198-107">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d198-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d198-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1d198-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1d198-109">Handle de la technique parente.</span><span class="sxs-lookup"><span data-stu-id="1d198-109">Handle of the parent technique.</span></span> <span data-ttu-id="1d198-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1d198-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d198-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d198-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d198-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d198-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d198-113">Chaîne contenant le nom du test.</span><span class="sxs-lookup"><span data-stu-id="1d198-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d198-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d198-114">Return value</span></span>

<span data-ttu-id="1d198-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1d198-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1d198-116">Retourne le handle de la première passe à l’intérieur de la technique spécifiée qui porte le nom spécifié, ou **null** si le nom est introuvable.</span><span class="sxs-lookup"><span data-stu-id="1d198-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="1d198-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1d198-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d198-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d198-118">Requirements</span></span>



| <span data-ttu-id="1d198-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d198-119">Requirement</span></span> | <span data-ttu-id="1d198-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d198-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d198-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d198-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1d198-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d198-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1d198-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d198-123">Library</span></span><br/> | <dl> <span data-ttu-id="1d198-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d198-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1d198-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d198-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d198-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1d198-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
