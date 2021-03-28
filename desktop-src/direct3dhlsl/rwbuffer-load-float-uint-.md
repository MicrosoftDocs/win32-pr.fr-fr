---
title: 'RWBuffer :: Load (int, uint), fonction'
description: 'Lit les données de mémoire tampon et retourne l’état de l’opération. | RWBuffer :: Load (int, uint), fonction'
ms.assetid: 90C9ECE8-2068-47C7-B87A-941B2D4F221D
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
ms.openlocfilehash: 81d23d67b0d02ed375e07f310089067d6a7bbd67
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116102"
---
# <a name="rwbufferloadintuint-function"></a><span data-ttu-id="fa6b7-105">RWBuffer :: Load (int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="fa6b7-105">RWBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="fa6b7-106">Lit les données de mémoire tampon et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6b7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa6b7-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="fa6b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa6b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa6b7-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa6b7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6b7-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="fa6b7-110">Type: **int**</span></span>

<span data-ttu-id="fa6b7-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fa6b7-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa6b7-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6b7-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="fa6b7-113">Type: **uint**</span></span>

<span data-ttu-id="fa6b7-114">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-114">The status of the operation.</span></span> <span data-ttu-id="fa6b7-115">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fa6b7-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fa6b7-116">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fa6b7-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fa6b7-117">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fa6b7-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa6b7-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa6b7-118">Return value</span></span>

<span data-ttu-id="fa6b7-119">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fa6b7-119">Type:</span></span>

<span data-ttu-id="fa6b7-120">Le type de retour correspond au type dans la déclaration pour l’objet [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fa6b7-120">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa6b7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fa6b7-121">Remarks</span></span>

<span data-ttu-id="fa6b7-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fa6b7-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fa6b7-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="fa6b7-123">Vertex</span></span> | <span data-ttu-id="fa6b7-124">Forme</span><span class="sxs-lookup"><span data-stu-id="fa6b7-124">Hull</span></span> | <span data-ttu-id="fa6b7-125">Domain</span><span class="sxs-lookup"><span data-stu-id="fa6b7-125">Domain</span></span> | <span data-ttu-id="fa6b7-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="fa6b7-126">Geometry</span></span> | <span data-ttu-id="fa6b7-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="fa6b7-127">Pixel</span></span> | <span data-ttu-id="fa6b7-128">Compute</span><span class="sxs-lookup"><span data-stu-id="fa6b7-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fa6b7-129">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-129">x</span></span>      | <span data-ttu-id="fa6b7-130">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-130">x</span></span>    | <span data-ttu-id="fa6b7-131">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-131">x</span></span>      | <span data-ttu-id="fa6b7-132">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-132">x</span></span>        | <span data-ttu-id="fa6b7-133">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-133">x</span></span>     | <span data-ttu-id="fa6b7-134">x</span><span class="sxs-lookup"><span data-stu-id="fa6b7-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fa6b7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa6b7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6b7-136">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="fa6b7-136">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 
