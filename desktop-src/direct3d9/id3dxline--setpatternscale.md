---
description: Étire le modèle stipple le long de la direction de la ligne.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine :: SetPatternScale, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211959"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="0c070-103">ID3DXLine :: SetPatternScale, méthode</span><span class="sxs-lookup"><span data-stu-id="0c070-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="0c070-104">Étire le modèle stipple le long de la direction de la ligne.</span><span class="sxs-lookup"><span data-stu-id="0c070-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c070-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c070-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="0c070-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c070-107">*fPatternScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c070-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c070-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c070-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c070-109">Valeur de mise à l’échelle du modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="0c070-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="0c070-110">1.0 f est la valeur par défaut et ne représente aucune mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="0c070-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="0c070-111">Une valeur inférieure à 1,0 f réduit le modèle, et une valeur supérieure à 1,0 étire le modèle.</span><span class="sxs-lookup"><span data-stu-id="0c070-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c070-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c070-112">Return value</span></span>

<span data-ttu-id="0c070-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c070-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c070-114">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c070-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c070-115">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="0c070-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c070-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c070-116">Requirements</span></span>



| <span data-ttu-id="0c070-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c070-117">Requirement</span></span> | <span data-ttu-id="0c070-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c070-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c070-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c070-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0c070-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c070-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0c070-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c070-121">Library</span></span><br/> | <dl> <span data-ttu-id="0c070-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c070-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c070-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c070-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c070-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="0c070-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
