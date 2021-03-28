---
title: Abort, fonction (Corecrt \_ Terminate. h)
description: Envoie un message d’erreur à la file d’attente d’informations et met fin à l’appel de dessin ou de distribution en cours d’exécution.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- fonction d’abandon HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982634"
---
# <a name="abort-function"></a><span data-ttu-id="2fa05-104">abort (fonction)</span><span class="sxs-lookup"><span data-stu-id="2fa05-104">abort function</span></span>

<span data-ttu-id="2fa05-105">Envoie un message d’erreur à la file d’attente d’informations et met fin à l’appel de dessin ou de distribution en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2fa05-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa05-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fa05-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="2fa05-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fa05-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="2fa05-108">None</span><span class="sxs-lookup"><span data-stu-id="2fa05-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa05-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2fa05-109">Return value</span></span>

<span data-ttu-id="2fa05-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2fa05-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa05-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2fa05-111">Remarks</span></span>

<span data-ttu-id="2fa05-112">Cette opération ne fait rien sur les rastériseurs qui ne la prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="2fa05-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2fa05-113">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2fa05-113">Minimum Shader Model</span></span>

<span data-ttu-id="2fa05-114">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="2fa05-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2fa05-115">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2fa05-115">Shader Model</span></span>                                                        | <span data-ttu-id="2fa05-116">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2fa05-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="2fa05-117">Shader Model 4 (DirectX HLSL) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2fa05-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fa05-118">Oui</span><span class="sxs-lookup"><span data-stu-id="2fa05-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="2fa05-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fa05-119">Requirements</span></span>



| <span data-ttu-id="2fa05-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fa05-120">Requirement</span></span> | <span data-ttu-id="2fa05-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fa05-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa05-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fa05-122">Header</span></span><br/> | <dl> <span data-ttu-id="2fa05-123"><dt>Corecrt \_ Terminate. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa05-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa05-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa05-125">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="2fa05-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





