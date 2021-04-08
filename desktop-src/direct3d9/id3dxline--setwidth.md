---
description: Spécifie l’épaisseur de la ligne.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'ID3DXLine :: SetWidth, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043170"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="f045e-103">ID3DXLine :: SetWidth, méthode</span><span class="sxs-lookup"><span data-stu-id="f045e-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="f045e-104">Spécifie l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="f045e-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="f045e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f045e-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="f045e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f045e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f045e-107">*fWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f045e-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f045e-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f045e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f045e-109">Décrit la largeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="f045e-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f045e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f045e-110">Return value</span></span>

<span data-ttu-id="f045e-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f045e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f045e-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f045e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f045e-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="f045e-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f045e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f045e-114">Requirements</span></span>



| <span data-ttu-id="f045e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f045e-115">Requirement</span></span> | <span data-ttu-id="f045e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f045e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f045e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f045e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f045e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f045e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f045e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f045e-119">Library</span></span><br/> | <dl> <span data-ttu-id="f045e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f045e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f045e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f045e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f045e-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="f045e-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
