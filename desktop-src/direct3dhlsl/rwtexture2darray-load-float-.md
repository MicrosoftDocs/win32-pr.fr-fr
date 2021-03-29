---
title: 'RWTexture2DArray :: Load (int), fonction'
description: 'Lit les données de texture. | RWTexture2DArray :: Load (int), fonction'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
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
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322173"
---
# <a name="rwtexture2darrayloadint-function"></a><span data-ttu-id="2bf4d-105">RWTexture2DArray :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="2bf4d-105">RWTexture2DArray::Load(int) function</span></span>

<span data-ttu-id="2bf4d-106">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="2bf4d-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf4d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bf4d-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="2bf4d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bf4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf4d-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bf4d-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf4d-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="2bf4d-110">Type: **int**</span></span>

<span data-ttu-id="2bf4d-111">Emplacement de la texture.</span><span class="sxs-lookup"><span data-stu-id="2bf4d-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf4d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bf4d-112">Return value</span></span>

<span data-ttu-id="2bf4d-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="2bf4d-113">Type:</span></span>

<span data-ttu-id="2bf4d-114">Le type de retour correspond au type dans la déclaration pour l’objet [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf4d-114">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf4d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2bf4d-115">Remarks</span></span>

<span data-ttu-id="2bf4d-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2bf4d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2bf4d-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="2bf4d-117">Vertex</span></span> | <span data-ttu-id="2bf4d-118">Forme</span><span class="sxs-lookup"><span data-stu-id="2bf4d-118">Hull</span></span> | <span data-ttu-id="2bf4d-119">Domain</span><span class="sxs-lookup"><span data-stu-id="2bf4d-119">Domain</span></span> | <span data-ttu-id="2bf4d-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2bf4d-120">Geometry</span></span> | <span data-ttu-id="2bf4d-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="2bf4d-121">Pixel</span></span> | <span data-ttu-id="2bf4d-122">Compute</span><span class="sxs-lookup"><span data-stu-id="2bf4d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2bf4d-123">x</span><span class="sxs-lookup"><span data-stu-id="2bf4d-123">x</span></span>     | <span data-ttu-id="2bf4d-124">x</span><span class="sxs-lookup"><span data-stu-id="2bf4d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2bf4d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bf4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf4d-126">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="2bf4d-126">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 




