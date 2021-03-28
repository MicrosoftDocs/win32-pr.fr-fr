---
title: 'Fonction buffer :: Load (int, uint)'
description: 'Lit les données de mémoire tampon et retourne l’état de l’opération. | Fonction buffer :: Load (int, uint)'
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
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
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973915"
---
# <a name="bufferloadint-uint-function"></a><span data-ttu-id="0f7eb-105">Fonction buffer :: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="0f7eb-105">Buffer::Load(int, uint) function</span></span>

<span data-ttu-id="0f7eb-106">Lit les données de mémoire tampon et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f7eb-107">Syntax</span></span>

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="0f7eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f7eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7eb-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f7eb-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7eb-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="0f7eb-110">Type: **int**</span></span>

<span data-ttu-id="0f7eb-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0f7eb-112">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0f7eb-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7eb-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="0f7eb-113">Type: **uint**</span></span>

<span data-ttu-id="0f7eb-114">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-114">The status of the operation.</span></span> <span data-ttu-id="0f7eb-115">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0f7eb-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0f7eb-116">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0f7eb-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0f7eb-117">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7eb-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f7eb-118">Return value</span></span>

<span data-ttu-id="0f7eb-119">Tapez :</span><span class="sxs-lookup"><span data-stu-id="0f7eb-119">Type:</span></span>

<span data-ttu-id="0f7eb-120">Le type de retour correspond au type dans la déclaration pour l’objet de [**mémoire tampon**](sm5-object-buffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0f7eb-120">The return type matches the type in the declaration for the [**Buffer**](sm5-object-buffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7eb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0f7eb-121">Remarks</span></span>

<span data-ttu-id="0f7eb-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0f7eb-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0f7eb-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="0f7eb-123">Vertex</span></span> | <span data-ttu-id="0f7eb-124">Forme</span><span class="sxs-lookup"><span data-stu-id="0f7eb-124">Hull</span></span> | <span data-ttu-id="0f7eb-125">Domain</span><span class="sxs-lookup"><span data-stu-id="0f7eb-125">Domain</span></span> | <span data-ttu-id="0f7eb-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0f7eb-126">Geometry</span></span> | <span data-ttu-id="0f7eb-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="0f7eb-127">Pixel</span></span> | <span data-ttu-id="0f7eb-128">Compute</span><span class="sxs-lookup"><span data-stu-id="0f7eb-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0f7eb-129">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-129">x</span></span>      | <span data-ttu-id="0f7eb-130">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-130">x</span></span>    | <span data-ttu-id="0f7eb-131">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-131">x</span></span>      | <span data-ttu-id="0f7eb-132">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-132">x</span></span>        | <span data-ttu-id="0f7eb-133">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-133">x</span></span>     | <span data-ttu-id="0f7eb-134">x</span><span class="sxs-lookup"><span data-stu-id="0f7eb-134">x</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="0f7eb-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="0f7eb-135">Examples</span></span>

<span data-ttu-id="0f7eb-136">Cet exemple montre comment utiliser **Load**:</span><span class="sxs-lookup"><span data-stu-id="0f7eb-136">This example shows how to use **Load**:</span></span>

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a><span data-ttu-id="0f7eb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f7eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7eb-138">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="0f7eb-138">Load methods</span></span>](buffer-load.md)
</dt> </dl>

 

 
