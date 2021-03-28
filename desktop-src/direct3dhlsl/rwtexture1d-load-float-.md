---
title: 'RWTexture1D :: Load (int), fonction'
description: 'Lit les données de texture. | RWTexture1D :: Load (int), fonction'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322222"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="8b6fc-105">RWTexture1D :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="8b6fc-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="8b6fc-106">Lit les données de texture.</span><span class="sxs-lookup"><span data-stu-id="8b6fc-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b6fc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b6fc-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="8b6fc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b6fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b6fc-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b6fc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b6fc-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="8b6fc-110">Type: **int**</span></span>

<span data-ttu-id="8b6fc-111">Emplacement de la texture.</span><span class="sxs-lookup"><span data-stu-id="8b6fc-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b6fc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b6fc-112">Return value</span></span>

<span data-ttu-id="8b6fc-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="8b6fc-113">Type:</span></span>

<span data-ttu-id="8b6fc-114">Le type de retour correspond au type dans la déclaration pour l’objet [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="8b6fc-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b6fc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8b6fc-115">Remarks</span></span>

<span data-ttu-id="8b6fc-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8b6fc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8b6fc-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="8b6fc-117">Vertex</span></span> | <span data-ttu-id="8b6fc-118">Forme</span><span class="sxs-lookup"><span data-stu-id="8b6fc-118">Hull</span></span> | <span data-ttu-id="8b6fc-119">Domain</span><span class="sxs-lookup"><span data-stu-id="8b6fc-119">Domain</span></span> | <span data-ttu-id="8b6fc-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8b6fc-120">Geometry</span></span> | <span data-ttu-id="8b6fc-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="8b6fc-121">Pixel</span></span> | <span data-ttu-id="8b6fc-122">Compute</span><span class="sxs-lookup"><span data-stu-id="8b6fc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8b6fc-123">x</span><span class="sxs-lookup"><span data-stu-id="8b6fc-123">x</span></span>     | <span data-ttu-id="8b6fc-124">x</span><span class="sxs-lookup"><span data-stu-id="8b6fc-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8b6fc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b6fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b6fc-126">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="8b6fc-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




