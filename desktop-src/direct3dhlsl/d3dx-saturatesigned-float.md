---
title: D3DX_SaturateSigned_FLOAT fonction)
description: Récupère une valeur saturée signée du FLOAT donné.
ms.assetid: 2737ea61-5dbf-4451-bb4f-436e6ea95db6
keywords:
- D3DX_SaturateSigned_FLOAT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_SaturateSigned_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e6ccf5cf941b1abd3577efa5899b8d827e24e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211832"
---
# <a name="d3dx_saturatesigned_float-function"></a><span data-ttu-id="89dbb-104">D3DX \_ SaturateSigned \_ float, fonction</span><span class="sxs-lookup"><span data-stu-id="89dbb-104">D3DX\_SaturateSigned\_FLOAT function</span></span>

<span data-ttu-id="89dbb-105">Récupère une valeur saturée signée du FLOAT donné.</span><span class="sxs-lookup"><span data-stu-id="89dbb-105">Retrieves a signed saturated value from the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="89dbb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89dbb-106">Syntax</span></span>

``` syntax
 D3DX_SaturateSigned_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="89dbb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89dbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89dbb-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="89dbb-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="89dbb-109">Valeur à saturer.</span><span class="sxs-lookup"><span data-stu-id="89dbb-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89dbb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89dbb-110">Return value</span></span>

<span data-ttu-id="89dbb-111">Valeur saturée signée.</span><span class="sxs-lookup"><span data-stu-id="89dbb-111">The signed saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89dbb-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="89dbb-112">Requirements</span></span>



| <span data-ttu-id="89dbb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89dbb-113">Requirement</span></span> | <span data-ttu-id="89dbb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="89dbb-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dbb-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="89dbb-115">Header</span></span><br/> | <dl> <span data-ttu-id="89dbb-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="89dbb-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89dbb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89dbb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89dbb-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="89dbb-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="89dbb-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="89dbb-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





