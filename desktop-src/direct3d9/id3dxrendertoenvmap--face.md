---
description: Initiez le dessin de chaque face d’une carte d’environnement.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap :: face, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762344"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="7d84e-103">ID3DXRenderToEnvMap :: face, méthode</span><span class="sxs-lookup"><span data-stu-id="7d84e-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="7d84e-104">Initiez le dessin de chaque face d’une carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="7d84e-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d84e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d84e-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="7d84e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d84e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d84e-107">*Visage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d84e-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d84e-108">Type : **[ **D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="7d84e-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="7d84e-109">Première face du mappage de cube environnemental.</span><span class="sxs-lookup"><span data-stu-id="7d84e-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="7d84e-110">Consultez [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md).</span><span class="sxs-lookup"><span data-stu-id="7d84e-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d84e-111">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d84e-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d84e-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d84e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d84e-113">Combinaison valide d’un ou plusieurs indicateurs [de \_ filtre D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7d84e-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d84e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d84e-114">Return value</span></span>

<span data-ttu-id="7d84e-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d84e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d84e-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7d84e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7d84e-117">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7d84e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d84e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7d84e-118">Remarks</span></span>

<span data-ttu-id="7d84e-119">Cette méthode doit être appelée une fois pour chaque type de carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="7d84e-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="7d84e-120">La seule exception est un mappage d’environnement cubique qui requiert que cette méthode soit appelée six fois, une fois pour chaque visage dans des \_ visages D3DCUBEMAP.</span><span class="sxs-lookup"><span data-stu-id="7d84e-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="7d84e-121">Pour plus d’informations, consultez [mappage d’environnement (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="7d84e-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d84e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d84e-122">Requirements</span></span>



| <span data-ttu-id="7d84e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d84e-123">Requirement</span></span> | <span data-ttu-id="7d84e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d84e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d84e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d84e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7d84e-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d84e-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7d84e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d84e-127">Library</span></span><br/> | <dl> <span data-ttu-id="7d84e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d84e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d84e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d84e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d84e-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="7d84e-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
