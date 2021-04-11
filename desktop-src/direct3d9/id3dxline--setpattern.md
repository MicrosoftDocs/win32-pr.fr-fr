---
description: Applique un modèle de stipple à la ligne.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'ID3DXLine :: SetPattern, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116274"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="062eb-103">ID3DXLine :: SetPattern, méthode</span><span class="sxs-lookup"><span data-stu-id="062eb-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="062eb-104">Applique un modèle de stipple à la ligne.</span><span class="sxs-lookup"><span data-stu-id="062eb-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="062eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="062eb-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="062eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="062eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062eb-107">*dwPattern* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="062eb-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062eb-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="062eb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="062eb-109">Décrit le modèle stipple : 1 est opaque, 0 est transparent.</span><span class="sxs-lookup"><span data-stu-id="062eb-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="062eb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="062eb-110">Return value</span></span>

<span data-ttu-id="062eb-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="062eb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="062eb-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="062eb-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="062eb-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="062eb-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="062eb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="062eb-114">Requirements</span></span>



| <span data-ttu-id="062eb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="062eb-115">Requirement</span></span> | <span data-ttu-id="062eb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="062eb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="062eb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="062eb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="062eb-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="062eb-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="062eb-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="062eb-119">Library</span></span><br/> | <dl> <span data-ttu-id="062eb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="062eb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="062eb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062eb-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="062eb-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
