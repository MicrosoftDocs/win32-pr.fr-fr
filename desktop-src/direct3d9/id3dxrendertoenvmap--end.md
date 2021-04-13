---
description: Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322802"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="0bc7b-103">ID3DXRenderToEnvMap :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="0bc7b-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="0bc7b-104">Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="0bc7b-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bc7b-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="0bc7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bc7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc7b-107">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bc7b-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc7b-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc7b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bc7b-109">Combinaison valide d’un ou plusieurs indicateurs [de \_ filtre D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0bc7b-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc7b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bc7b-110">Return value</span></span>

<span data-ttu-id="0bc7b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bc7b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bc7b-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc7b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0bc7b-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0bc7b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc7b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bc7b-114">Requirements</span></span>



| <span data-ttu-id="0bc7b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bc7b-115">Requirement</span></span> | <span data-ttu-id="0bc7b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc7b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc7b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bc7b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc7b-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc7b-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc7b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bc7b-119">Library</span></span><br/> | <dl> <span data-ttu-id="0bc7b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc7b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bc7b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bc7b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc7b-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="0bc7b-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="0bc7b-123">**ID3DXRenderToEnvMap :: face**</span><span class="sxs-lookup"><span data-stu-id="0bc7b-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
