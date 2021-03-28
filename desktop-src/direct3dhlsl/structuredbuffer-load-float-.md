---
title: 'StructuredBuffer :: Load (int), fonction'
description: 'Lit les données de la mémoire tampon. | StructuredBuffer :: Load (int), fonction'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974322"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="56158-105">StructuredBuffer :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="56158-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="56158-106">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="56158-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="56158-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56158-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="56158-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56158-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56158-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56158-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56158-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="56158-110">Type: **int**</span></span>

<span data-ttu-id="56158-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="56158-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56158-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56158-112">Return value</span></span>

<span data-ttu-id="56158-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="56158-113">Type:</span></span>

<span data-ttu-id="56158-114">Le type de retour correspond au type dans la déclaration pour l’objet [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="56158-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56158-115">Notes</span><span class="sxs-lookup"><span data-stu-id="56158-115">Remarks</span></span>

<span data-ttu-id="56158-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="56158-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56158-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="56158-117">Vertex</span></span> | <span data-ttu-id="56158-118">Forme</span><span class="sxs-lookup"><span data-stu-id="56158-118">Hull</span></span> | <span data-ttu-id="56158-119">Domain</span><span class="sxs-lookup"><span data-stu-id="56158-119">Domain</span></span> | <span data-ttu-id="56158-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="56158-120">Geometry</span></span> | <span data-ttu-id="56158-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="56158-121">Pixel</span></span> | <span data-ttu-id="56158-122">Compute</span><span class="sxs-lookup"><span data-stu-id="56158-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="56158-123">x</span><span class="sxs-lookup"><span data-stu-id="56158-123">x</span></span>     | <span data-ttu-id="56158-124">x</span><span class="sxs-lookup"><span data-stu-id="56158-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56158-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56158-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56158-126">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="56158-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




