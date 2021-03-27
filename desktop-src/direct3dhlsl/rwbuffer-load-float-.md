---
title: 'RWBuffer :: Load (int), fonction'
description: 'Lit les données de la mémoire tampon. | RWBuffer :: Load (int), fonction'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761690"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="ecd5c-105">RWBuffer :: Load (int), fonction</span><span class="sxs-lookup"><span data-stu-id="ecd5c-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="ecd5c-106">Lit les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd5c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecd5c-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="ecd5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecd5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd5c-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ecd5c-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd5c-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="ecd5c-110">Type: **int**</span></span>

<span data-ttu-id="ecd5c-111">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd5c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ecd5c-112">Return value</span></span>

<span data-ttu-id="ecd5c-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="ecd5c-113">Type:</span></span>

<span data-ttu-id="ecd5c-114">Le type de retour correspond au type dans la déclaration pour l’objet [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd5c-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd5c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ecd5c-115">Remarks</span></span>

<span data-ttu-id="ecd5c-116">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ecd5c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ecd5c-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="ecd5c-117">Vertex</span></span> | <span data-ttu-id="ecd5c-118">Forme</span><span class="sxs-lookup"><span data-stu-id="ecd5c-118">Hull</span></span> | <span data-ttu-id="ecd5c-119">Domain</span><span class="sxs-lookup"><span data-stu-id="ecd5c-119">Domain</span></span> | <span data-ttu-id="ecd5c-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ecd5c-120">Geometry</span></span> | <span data-ttu-id="ecd5c-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="ecd5c-121">Pixel</span></span> | <span data-ttu-id="ecd5c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="ecd5c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ecd5c-123">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-123">x</span></span>      | <span data-ttu-id="ecd5c-124">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-124">x</span></span>    | <span data-ttu-id="ecd5c-125">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-125">x</span></span>      | <span data-ttu-id="ecd5c-126">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-126">x</span></span>        | <span data-ttu-id="ecd5c-127">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-127">x</span></span>     | <span data-ttu-id="ecd5c-128">x</span><span class="sxs-lookup"><span data-stu-id="ecd5c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ecd5c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd5c-130">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="ecd5c-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




