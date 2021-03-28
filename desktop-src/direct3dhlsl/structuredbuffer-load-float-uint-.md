---
title: 'StructuredBuffer :: Load (int, uint), fonction'
description: 'Lit les données de mémoire tampon et retourne l’état de l’opération. | StructuredBuffer :: Load (int, uint), fonction'
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 957b85631bbd19742cb7afe52f6bf061de323614
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211474"
---
# <a name="structuredbufferloadintuint-function"></a><span data-ttu-id="647cc-105">StructuredBuffer :: Load (int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="647cc-105">StructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="647cc-106">Lit les données de mémoire tampon et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="647cc-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="647cc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="647cc-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="647cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="647cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647cc-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="647cc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647cc-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="647cc-110">Type: **int**</span></span>

<span data-ttu-id="647cc-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="647cc-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="647cc-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="647cc-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="647cc-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="647cc-113">Type: **uint**</span></span>

<span data-ttu-id="647cc-114">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="647cc-114">The status of the operation.</span></span> <span data-ttu-id="647cc-115">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="647cc-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="647cc-116">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="647cc-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="647cc-117">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="647cc-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647cc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="647cc-118">Return value</span></span>

<span data-ttu-id="647cc-119">Tapez :</span><span class="sxs-lookup"><span data-stu-id="647cc-119">Type:</span></span>

<span data-ttu-id="647cc-120">Le type de retour correspond au type dans la déclaration pour l’objet [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="647cc-120">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="647cc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="647cc-121">Remarks</span></span>

<span data-ttu-id="647cc-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="647cc-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="647cc-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="647cc-123">Vertex</span></span> | <span data-ttu-id="647cc-124">Forme</span><span class="sxs-lookup"><span data-stu-id="647cc-124">Hull</span></span> | <span data-ttu-id="647cc-125">Domain</span><span class="sxs-lookup"><span data-stu-id="647cc-125">Domain</span></span> | <span data-ttu-id="647cc-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="647cc-126">Geometry</span></span> | <span data-ttu-id="647cc-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="647cc-127">Pixel</span></span> | <span data-ttu-id="647cc-128">Compute</span><span class="sxs-lookup"><span data-stu-id="647cc-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="647cc-129">x</span><span class="sxs-lookup"><span data-stu-id="647cc-129">x</span></span>     | <span data-ttu-id="647cc-130">x</span><span class="sxs-lookup"><span data-stu-id="647cc-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="647cc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="647cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647cc-132">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="647cc-132">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 
