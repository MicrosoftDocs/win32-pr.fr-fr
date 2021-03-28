---
title: 'ConsumeStructuredBuffer :: consume, fonction'
description: Supprime une valeur à partir de la fin de la mémoire tampon.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Utiliser la fonction HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030483"
---
# <a name="consume-function"></a><span data-ttu-id="bd45a-104">Consume (fonction)</span><span class="sxs-lookup"><span data-stu-id="bd45a-104">Consume function</span></span>

<span data-ttu-id="bd45a-105">Supprime une valeur à partir de la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bd45a-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd45a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd45a-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="bd45a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd45a-107">Parameters</span></span>

<span data-ttu-id="bd45a-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="bd45a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd45a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd45a-109">Return value</span></span>

<span data-ttu-id="bd45a-110">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="bd45a-110">Type: **T**</span></span>

<span data-ttu-id="bd45a-111">La valeur supprimée (peut être une structure).</span><span class="sxs-lookup"><span data-stu-id="bd45a-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd45a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bd45a-112">Remarks</span></span>

<span data-ttu-id="bd45a-113">T peut être n’importe quel type de données, y compris une structure.</span><span class="sxs-lookup"><span data-stu-id="bd45a-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="bd45a-114">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="bd45a-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bd45a-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="bd45a-115">Vertex</span></span> | <span data-ttu-id="bd45a-116">Forme</span><span class="sxs-lookup"><span data-stu-id="bd45a-116">Hull</span></span> | <span data-ttu-id="bd45a-117">Domain</span><span class="sxs-lookup"><span data-stu-id="bd45a-117">Domain</span></span> | <span data-ttu-id="bd45a-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bd45a-118">Geometry</span></span> | <span data-ttu-id="bd45a-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="bd45a-119">Pixel</span></span> | <span data-ttu-id="bd45a-120">Compute</span><span class="sxs-lookup"><span data-stu-id="bd45a-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bd45a-121">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-121">x</span></span>      | <span data-ttu-id="bd45a-122">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-122">x</span></span>    | <span data-ttu-id="bd45a-123">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-123">x</span></span>      | <span data-ttu-id="bd45a-124">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-124">x</span></span>        | <span data-ttu-id="bd45a-125">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-125">x</span></span>     | <span data-ttu-id="bd45a-126">x</span><span class="sxs-lookup"><span data-stu-id="bd45a-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bd45a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd45a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd45a-128">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="bd45a-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="bd45a-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="bd45a-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




