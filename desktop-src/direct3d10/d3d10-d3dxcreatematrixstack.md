---
description: Créer une pile de matrice.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: D3DXCreateMatrixStack, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394204"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="5c847-103">D3DXCreateMatrixStack, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5c847-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="5c847-104">Créer une pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="5c847-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c847-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c847-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="5c847-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c847-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5c847-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c847-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c847-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c847-109">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="5c847-109">Not implemented.</span></span> <span data-ttu-id="5c847-110">Spécifiez zéro.</span><span class="sxs-lookup"><span data-stu-id="5c847-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c847-111">*ppStack* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c847-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c847-112">Type : **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="5c847-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="5c847-113">Adresse d’un pointeur vers une pile de matrice (voir [**interface ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="5c847-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c847-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c847-114">Return value</span></span>

<span data-ttu-id="5c847-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c847-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c847-116">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5c847-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c847-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c847-117">Requirements</span></span>



| <span data-ttu-id="5c847-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c847-118">Requirement</span></span> | <span data-ttu-id="5c847-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c847-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c847-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c847-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5c847-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c847-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5c847-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5c847-122">Library</span></span><br/> | <dl> <span data-ttu-id="5c847-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c847-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c847-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c847-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c847-125">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5c847-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
