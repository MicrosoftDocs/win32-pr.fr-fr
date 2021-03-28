---
title: 'RWTexture1D :: Load (int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | RWTexture1D :: Load (int, uint), fonction'
ms.assetid: 3BF2397D-400C-48EE-8D45-872BA61F007B
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
ms.openlocfilehash: afba9445d152810e5776ae0ee7f603bb7ee55ac2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973995"
---
# <a name="rwtexture1dloadintuint-function"></a><span data-ttu-id="bec33-105">RWTexture1D :: Load (int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="bec33-105">RWTexture1D::Load(int,uint) function</span></span>

<span data-ttu-id="bec33-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bec33-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec33-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bec33-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="bec33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bec33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec33-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bec33-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec33-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="bec33-110">Type: **int**</span></span>

<span data-ttu-id="bec33-111">Emplacement de la texture.</span><span class="sxs-lookup"><span data-stu-id="bec33-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="bec33-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bec33-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bec33-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="bec33-113">Type: **uint**</span></span>

<span data-ttu-id="bec33-114">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bec33-114">The status of the operation.</span></span> <span data-ttu-id="bec33-115">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="bec33-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bec33-116">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="bec33-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bec33-117">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="bec33-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec33-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bec33-118">Return value</span></span>

<span data-ttu-id="bec33-119">Tapez :</span><span class="sxs-lookup"><span data-stu-id="bec33-119">Type:</span></span>

<span data-ttu-id="bec33-120">Le type de retour correspond au type dans la déclaration pour l’objet [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="bec33-120">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec33-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bec33-121">Remarks</span></span>

<span data-ttu-id="bec33-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="bec33-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bec33-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="bec33-123">Vertex</span></span> | <span data-ttu-id="bec33-124">Forme</span><span class="sxs-lookup"><span data-stu-id="bec33-124">Hull</span></span> | <span data-ttu-id="bec33-125">Domain</span><span class="sxs-lookup"><span data-stu-id="bec33-125">Domain</span></span> | <span data-ttu-id="bec33-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bec33-126">Geometry</span></span> | <span data-ttu-id="bec33-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="bec33-127">Pixel</span></span> | <span data-ttu-id="bec33-128">Compute</span><span class="sxs-lookup"><span data-stu-id="bec33-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bec33-129">x</span><span class="sxs-lookup"><span data-stu-id="bec33-129">x</span></span>     | <span data-ttu-id="bec33-130">x</span><span class="sxs-lookup"><span data-stu-id="bec33-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bec33-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bec33-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec33-132">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="bec33-132">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 
