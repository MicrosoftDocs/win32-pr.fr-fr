---
description: Active ou désactive l’anticrénelage de ligne.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine :: SetAntialias, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538555"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="e78e6-103">ID3DXLine :: SetAntialias, méthode</span><span class="sxs-lookup"><span data-stu-id="e78e6-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="e78e6-104">Active ou désactive l’anticrénelage de ligne.</span><span class="sxs-lookup"><span data-stu-id="e78e6-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e78e6-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="e78e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e78e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78e6-107">*bAntiAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e78e6-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78e6-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e78e6-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e78e6-109">Active ou désactive l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="e78e6-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="e78e6-110">**True** active l’anticrénelage et **false** désactive l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="e78e6-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e78e6-111">Return value</span></span>

<span data-ttu-id="e78e6-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e78e6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e78e6-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e78e6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e78e6-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="e78e6-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e78e6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e78e6-115">Requirements</span></span>



| <span data-ttu-id="e78e6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e78e6-116">Requirement</span></span> | <span data-ttu-id="e78e6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e78e6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e78e6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e78e6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e78e6-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e78e6-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e78e6-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e78e6-120">Library</span></span><br/> | <dl> <span data-ttu-id="e78e6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e78e6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e78e6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e78e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78e6-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="e78e6-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="e78e6-124">**ID3DXLine::GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="e78e6-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
