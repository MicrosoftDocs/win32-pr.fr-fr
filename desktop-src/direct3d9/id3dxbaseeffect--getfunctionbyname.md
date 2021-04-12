---
description: Obtient le handle d’une fonction en recherchant son nom.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'ID3DXBaseEffect :: GetFunctionByName, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323341"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="22b5e-103">ID3DXBaseEffect :: GetFunctionByName, méthode</span><span class="sxs-lookup"><span data-stu-id="22b5e-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="22b5e-104">Obtient le handle d’une fonction en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="22b5e-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b5e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22b5e-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="22b5e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22b5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b5e-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22b5e-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b5e-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22b5e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22b5e-109">Chaîne contenant le nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="22b5e-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b5e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22b5e-110">Return value</span></span>

<span data-ttu-id="22b5e-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22b5e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22b5e-112">Retourne le handle de la fonction spécifiée, ou **null** si le nom est introuvable.</span><span class="sxs-lookup"><span data-stu-id="22b5e-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="22b5e-113">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="22b5e-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22b5e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22b5e-114">Requirements</span></span>



| <span data-ttu-id="22b5e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22b5e-115">Requirement</span></span> | <span data-ttu-id="22b5e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="22b5e-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b5e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="22b5e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22b5e-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b5e-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="22b5e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22b5e-119">Library</span></span><br/> | <dl> <span data-ttu-id="22b5e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b5e-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22b5e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22b5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b5e-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="22b5e-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
