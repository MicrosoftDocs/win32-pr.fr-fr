---
title: 'RWStructuredBuffer :: Load (int), fonction'
description: 'Lit les données de la mémoire tampon. | RWStructuredBuffer :: Load (int), fonction'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
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
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991905"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="c1a17-105">RWStructuredBuffer :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="c1a17-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="c1a17-106">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1a17-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1a17-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="c1a17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a17-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1a17-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a17-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c1a17-110">Type: **int**</span></span>

<span data-ttu-id="c1a17-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1a17-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a17-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1a17-112">Return value</span></span>

<span data-ttu-id="c1a17-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="c1a17-113">Type:</span></span>

<span data-ttu-id="c1a17-114">Le type de retour correspond au type dans la déclaration pour l’objet [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a17-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a17-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c1a17-115">Remarks</span></span>

<span data-ttu-id="c1a17-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c1a17-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c1a17-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="c1a17-117">Vertex</span></span> | <span data-ttu-id="c1a17-118">Forme</span><span class="sxs-lookup"><span data-stu-id="c1a17-118">Hull</span></span> | <span data-ttu-id="c1a17-119">Domain</span><span class="sxs-lookup"><span data-stu-id="c1a17-119">Domain</span></span> | <span data-ttu-id="c1a17-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c1a17-120">Geometry</span></span> | <span data-ttu-id="c1a17-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="c1a17-121">Pixel</span></span> | <span data-ttu-id="c1a17-122">Compute</span><span class="sxs-lookup"><span data-stu-id="c1a17-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c1a17-123">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-123">x</span></span>      | <span data-ttu-id="c1a17-124">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-124">x</span></span>    | <span data-ttu-id="c1a17-125">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-125">x</span></span>      | <span data-ttu-id="c1a17-126">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-126">x</span></span>        | <span data-ttu-id="c1a17-127">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-127">x</span></span>     | <span data-ttu-id="c1a17-128">x</span><span class="sxs-lookup"><span data-stu-id="c1a17-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1a17-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a17-130">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="c1a17-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




