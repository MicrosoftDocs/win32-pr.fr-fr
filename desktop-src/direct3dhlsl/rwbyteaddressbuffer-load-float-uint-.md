---
title: 'RWByteAddressBuffer :: Load (int, uint), fonction'
description: Obtient une valeur et retourne l’état de l’opération.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
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
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842933"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="7894b-104">RWByteAddressBuffer :: Load (int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="7894b-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="7894b-105">Obtient une valeur et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7894b-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7894b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7894b-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="7894b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7894b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7894b-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7894b-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7894b-109">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="7894b-109">Type: **int**</span></span>

<span data-ttu-id="7894b-110">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7894b-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7894b-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7894b-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7894b-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7894b-112">Type: **uint**</span></span>

<span data-ttu-id="7894b-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7894b-113">The status of the operation.</span></span> <span data-ttu-id="7894b-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7894b-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7894b-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7894b-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7894b-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="7894b-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7894b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7894b-117">Return value</span></span>

<span data-ttu-id="7894b-118">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7894b-118">Type: **uint**</span></span>

<span data-ttu-id="7894b-119">Une valeur.</span><span class="sxs-lookup"><span data-stu-id="7894b-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7894b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="7894b-120">Remarks</span></span>

<span data-ttu-id="7894b-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="7894b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7894b-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="7894b-122">Vertex</span></span> | <span data-ttu-id="7894b-123">Forme</span><span class="sxs-lookup"><span data-stu-id="7894b-123">Hull</span></span> | <span data-ttu-id="7894b-124">Domain</span><span class="sxs-lookup"><span data-stu-id="7894b-124">Domain</span></span> | <span data-ttu-id="7894b-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7894b-125">Geometry</span></span> | <span data-ttu-id="7894b-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="7894b-126">Pixel</span></span> | <span data-ttu-id="7894b-127">Compute</span><span class="sxs-lookup"><span data-stu-id="7894b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7894b-128">x</span><span class="sxs-lookup"><span data-stu-id="7894b-128">x</span></span>     | <span data-ttu-id="7894b-129">x</span><span class="sxs-lookup"><span data-stu-id="7894b-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7894b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7894b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7894b-131">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="7894b-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
