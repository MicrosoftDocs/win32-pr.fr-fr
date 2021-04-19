---
description: Retourne le niveau du pilote.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: D3DXGetDriverLevel, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523187"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="16122-103">D3DXGetDriverLevel fonction)</span><span class="sxs-lookup"><span data-stu-id="16122-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="16122-104">Retourne le niveau du pilote.</span><span class="sxs-lookup"><span data-stu-id="16122-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="16122-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16122-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="16122-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16122-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16122-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16122-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16122-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="16122-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="16122-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) représentant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="16122-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16122-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16122-110">Return value</span></span>

<span data-ttu-id="16122-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16122-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16122-112">Niveau du pilote.</span><span class="sxs-lookup"><span data-stu-id="16122-112">The driver level.</span></span> <span data-ttu-id="16122-113">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="16122-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="16122-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16122-114">Remarks</span></span>

<span data-ttu-id="16122-115">Cette méthode retourne la version du pilote, qui est l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="16122-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="16122-116">700-pilote de niveau Direct3D 7</span><span class="sxs-lookup"><span data-stu-id="16122-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="16122-117">800-pilote de niveau Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="16122-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="16122-118">900-pilote de niveau Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="16122-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="16122-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16122-119">Requirements</span></span>



| <span data-ttu-id="16122-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16122-120">Requirement</span></span> | <span data-ttu-id="16122-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16122-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16122-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="16122-122">Header</span></span><br/>  | <dl> <span data-ttu-id="16122-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="16122-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="16122-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16122-124">Library</span></span><br/> | <dl> <span data-ttu-id="16122-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16122-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16122-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16122-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16122-127">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="16122-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
