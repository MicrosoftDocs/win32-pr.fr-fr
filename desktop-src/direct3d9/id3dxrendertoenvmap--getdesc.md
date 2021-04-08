---
description: Récupère la description de la surface de rendu.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap :: GetDesc, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761996"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="18afc-103">ID3DXRenderToEnvMap :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="18afc-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="18afc-104">Récupère la description de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="18afc-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="18afc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18afc-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="18afc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18afc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18afc-107">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18afc-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18afc-108">Type : **[ **D3DXRTE \_ desc**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="18afc-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="18afc-109">Pointeur vers une structure [**D3DXRTE \_ desc**](d3dxrte-desc.md) qui décrit la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="18afc-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18afc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18afc-110">Return value</span></span>

<span data-ttu-id="18afc-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18afc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18afc-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18afc-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18afc-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="18afc-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="18afc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18afc-114">Requirements</span></span>



| <span data-ttu-id="18afc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18afc-115">Requirement</span></span> | <span data-ttu-id="18afc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="18afc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18afc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="18afc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="18afc-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="18afc-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="18afc-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18afc-119">Library</span></span><br/> | <dl> <span data-ttu-id="18afc-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18afc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18afc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18afc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18afc-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="18afc-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




