---
title: 'RWTexture1DArray :: Load (int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | RWTexture1DArray :: Load (int, uint), fonction'
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973991"
---
# <a name="rwtexture1darrayloadintuint-function"></a><span data-ttu-id="34d87-105">RWTexture1DArray :: Load (int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="34d87-105">RWTexture1DArray::Load(int,uint) function</span></span>

<span data-ttu-id="34d87-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="34d87-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d87-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="34d87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34d87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34d87-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34d87-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d87-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="34d87-110">Type: **int**</span></span>

<span data-ttu-id="34d87-111">Emplacement de la texture.</span><span class="sxs-lookup"><span data-stu-id="34d87-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="34d87-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34d87-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34d87-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="34d87-113">Type: **uint**</span></span>

<span data-ttu-id="34d87-114">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="34d87-114">The status of the operation.</span></span> <span data-ttu-id="34d87-115">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="34d87-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="34d87-116">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="34d87-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="34d87-117">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="34d87-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34d87-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34d87-118">Return value</span></span>

<span data-ttu-id="34d87-119">Tapez :</span><span class="sxs-lookup"><span data-stu-id="34d87-119">Type:</span></span>

<span data-ttu-id="34d87-120">Le type de retour correspond au type dans la déclaration pour l’objet [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="34d87-120">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d87-121">Notes</span><span class="sxs-lookup"><span data-stu-id="34d87-121">Remarks</span></span>

<span data-ttu-id="34d87-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="34d87-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="34d87-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="34d87-123">Vertex</span></span> | <span data-ttu-id="34d87-124">Forme</span><span class="sxs-lookup"><span data-stu-id="34d87-124">Hull</span></span> | <span data-ttu-id="34d87-125">Domain</span><span class="sxs-lookup"><span data-stu-id="34d87-125">Domain</span></span> | <span data-ttu-id="34d87-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="34d87-126">Geometry</span></span> | <span data-ttu-id="34d87-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="34d87-127">Pixel</span></span> | <span data-ttu-id="34d87-128">Compute</span><span class="sxs-lookup"><span data-stu-id="34d87-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="34d87-129">x</span><span class="sxs-lookup"><span data-stu-id="34d87-129">x</span></span>     | <span data-ttu-id="34d87-130">x</span><span class="sxs-lookup"><span data-stu-id="34d87-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="34d87-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34d87-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d87-132">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="34d87-132">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 
