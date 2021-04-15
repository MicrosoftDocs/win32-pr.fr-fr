---
description: Obtient la valeur de mise à l’échelle du modèle stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine :: GetPatternScale, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394263"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="7c76f-103">ID3DXLine :: GetPatternScale, méthode</span><span class="sxs-lookup"><span data-stu-id="7c76f-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="7c76f-104">Obtient la valeur de mise à l’échelle du modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="7c76f-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c76f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c76f-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="7c76f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c76f-106">Parameters</span></span>

<span data-ttu-id="7c76f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c76f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c76f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c76f-108">Return value</span></span>

<span data-ttu-id="7c76f-109">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c76f-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c76f-110">Retourne la valeur utilisée pour mettre à l’échelle le modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="7c76f-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="7c76f-111">1.0 f est la valeur par défaut et ne représente aucune mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="7c76f-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="7c76f-112">Une valeur inférieure à 1,0 f réduit le modèle, et une valeur supérieure à 1,0 étire le modèle.</span><span class="sxs-lookup"><span data-stu-id="7c76f-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c76f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c76f-113">Requirements</span></span>



| <span data-ttu-id="7c76f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c76f-114">Requirement</span></span> | <span data-ttu-id="7c76f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c76f-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c76f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c76f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7c76f-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c76f-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7c76f-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c76f-118">Library</span></span><br/> | <dl> <span data-ttu-id="7c76f-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c76f-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c76f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c76f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c76f-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="7c76f-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="7c76f-122">**ID3DXLine::SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="7c76f-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
