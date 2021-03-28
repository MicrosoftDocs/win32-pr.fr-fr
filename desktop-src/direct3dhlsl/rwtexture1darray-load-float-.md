---
title: 'RWTexture1DArray :: Load (int), fonction'
description: 'Lit les données de texture. | RWTexture1DArray :: Load (int), fonction'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973994"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="543eb-105">RWTexture1DArray :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="543eb-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="543eb-106">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="543eb-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="543eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="543eb-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="543eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="543eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543eb-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="543eb-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="543eb-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="543eb-110">Type: **int**</span></span>

<span data-ttu-id="543eb-111">Emplacement de la texture.</span><span class="sxs-lookup"><span data-stu-id="543eb-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="543eb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="543eb-112">Return value</span></span>

<span data-ttu-id="543eb-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="543eb-113">Type:</span></span>

<span data-ttu-id="543eb-114">Le type de retour correspond au type dans la déclaration pour l’objet [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="543eb-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="543eb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="543eb-115">Remarks</span></span>

<span data-ttu-id="543eb-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="543eb-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="543eb-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="543eb-117">Vertex</span></span> | <span data-ttu-id="543eb-118">Forme</span><span class="sxs-lookup"><span data-stu-id="543eb-118">Hull</span></span> | <span data-ttu-id="543eb-119">Domain</span><span class="sxs-lookup"><span data-stu-id="543eb-119">Domain</span></span> | <span data-ttu-id="543eb-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="543eb-120">Geometry</span></span> | <span data-ttu-id="543eb-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="543eb-121">Pixel</span></span> | <span data-ttu-id="543eb-122">Compute</span><span class="sxs-lookup"><span data-stu-id="543eb-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="543eb-123">x</span><span class="sxs-lookup"><span data-stu-id="543eb-123">x</span></span>     | <span data-ttu-id="543eb-124">x</span><span class="sxs-lookup"><span data-stu-id="543eb-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="543eb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="543eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="543eb-126">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="543eb-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




