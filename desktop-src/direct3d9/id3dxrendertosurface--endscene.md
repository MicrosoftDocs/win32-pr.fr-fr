---
description: Termine une scène.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'ID3DXRenderToSurface :: EndScene, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761995"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="7126e-103">ID3DXRenderToSurface :: EndScene, méthode</span><span class="sxs-lookup"><span data-stu-id="7126e-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="7126e-104">Termine une scène.</span><span class="sxs-lookup"><span data-stu-id="7126e-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="7126e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7126e-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="7126e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7126e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7126e-107">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7126e-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7126e-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7126e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7126e-109">Options de filtre, énumérées dans le [ \_ filtre D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7126e-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7126e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7126e-110">Return value</span></span>

<span data-ttu-id="7126e-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7126e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7126e-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7126e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7126e-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="7126e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="7126e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7126e-114">Requirements</span></span>



| <span data-ttu-id="7126e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7126e-115">Requirement</span></span> | <span data-ttu-id="7126e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7126e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7126e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7126e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7126e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7126e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7126e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7126e-119">Library</span></span><br/> | <dl> <span data-ttu-id="7126e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7126e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7126e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7126e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7126e-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="7126e-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="7126e-123">**ID3DXRenderToSurface::BeginScene**</span><span class="sxs-lookup"><span data-stu-id="7126e-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
