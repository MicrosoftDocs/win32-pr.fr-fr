---
title: D3DX_FLOAT_to_INT fonction)
description: Convertit une valeur FLOAT en INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531065"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="f5de9-104">\_Fonction D3DX float \_ to \_ int</span><span class="sxs-lookup"><span data-stu-id="f5de9-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="f5de9-105">Convertit une valeur FLOAT en INT.</span><span class="sxs-lookup"><span data-stu-id="f5de9-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5de9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5de9-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="f5de9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5de9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5de9-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="f5de9-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="f5de9-109">Valeur v.</span><span class="sxs-lookup"><span data-stu-id="f5de9-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="f5de9-110">*\_Échelle*</span><span class="sxs-lookup"><span data-stu-id="f5de9-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="f5de9-111">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="f5de9-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5de9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5de9-112">Return value</span></span>

<span data-ttu-id="f5de9-113">Valeur FLOAT convertie</span><span class="sxs-lookup"><span data-stu-id="f5de9-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="f5de9-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f5de9-114">Requirements</span></span>



| <span data-ttu-id="f5de9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5de9-115">Requirement</span></span> | <span data-ttu-id="f5de9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5de9-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5de9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5de9-117">Header</span></span><br/> | <dl> <span data-ttu-id="f5de9-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="f5de9-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5de9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5de9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5de9-120">Fonctions</span><span class="sxs-lookup"><span data-stu-id="f5de9-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f5de9-121">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="f5de9-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





