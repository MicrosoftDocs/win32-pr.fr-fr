---
description: Obtient le handle d’une fonction.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'ID3DXBaseEffect :: GetFunction, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525097"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="17661-103">ID3DXBaseEffect :: GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="17661-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="17661-104">Obtient le handle d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="17661-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="17661-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17661-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="17661-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17661-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17661-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17661-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17661-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17661-109">Index de fonction.</span><span class="sxs-lookup"><span data-stu-id="17661-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17661-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17661-110">Return value</span></span>

<span data-ttu-id="17661-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="17661-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="17661-112">Retourne le handle de la fonction spécifiée, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17661-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="17661-113">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="17661-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17661-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17661-114">Requirements</span></span>



| <span data-ttu-id="17661-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17661-115">Requirement</span></span> | <span data-ttu-id="17661-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="17661-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17661-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="17661-117">Header</span></span><br/>  | <dl> <span data-ttu-id="17661-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="17661-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="17661-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17661-119">Library</span></span><br/> | <dl> <span data-ttu-id="17661-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17661-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17661-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17661-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17661-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="17661-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
