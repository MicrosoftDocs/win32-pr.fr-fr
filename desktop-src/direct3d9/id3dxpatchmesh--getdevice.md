---
description: Obtient l’appareil qui a créé le maillage.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'ID3DXPatchMesh :: GetDevice, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953986"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="ac0ac-103">ID3DXPatchMesh :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="ac0ac-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="ac0ac-104">Obtient l’appareil qui a créé le maillage.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac0ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac0ac-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ac0ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac0ac-107">*ppDevice* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ac0ac-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ac-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ac0ac-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ac0ac-109">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac0ac-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac0ac-110">Return value</span></span>

<span data-ttu-id="ac0ac-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac0ac-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac0ac-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac0ac-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0ac-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac0ac-114">Requirements</span></span>



| <span data-ttu-id="ac0ac-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac0ac-115">Requirement</span></span> | <span data-ttu-id="ac0ac-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac0ac-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0ac-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac0ac-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ac0ac-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ac-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ac0ac-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac0ac-119">Library</span></span><br/> | <dl> <span data-ttu-id="ac0ac-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ac-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac0ac-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac0ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0ac-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ac0ac-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
