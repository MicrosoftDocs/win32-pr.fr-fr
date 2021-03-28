---
title: errorf fonction)
description: Envoie un message d’erreur à la file d’attente d’informations.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf fonction HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030098"
---
# <a name="errorf-function"></a><span data-ttu-id="6af3f-104">errorf fonction)</span><span class="sxs-lookup"><span data-stu-id="6af3f-104">errorf function</span></span>

<span data-ttu-id="6af3f-105">Envoie un message d’erreur à la file d’attente d’informations.</span><span class="sxs-lookup"><span data-stu-id="6af3f-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af3f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6af3f-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="6af3f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6af3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af3f-108">*format*</span><span class="sxs-lookup"><span data-stu-id="6af3f-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="6af3f-109">Chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="6af3f-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-110">*argument...*</span><span class="sxs-lookup"><span data-stu-id="6af3f-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="6af3f-111">Arguments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="6af3f-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af3f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6af3f-112">Return value</span></span>

<span data-ttu-id="6af3f-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6af3f-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af3f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6af3f-114">Remarks</span></span>

<span data-ttu-id="6af3f-115">Cette opération ne fait rien sur les appareils qui ne la prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="6af3f-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6af3f-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6af3f-116">Minimum Shader Model</span></span>

<span data-ttu-id="6af3f-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6af3f-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6af3f-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6af3f-118">Shader Model</span></span>                                                        | <span data-ttu-id="6af3f-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6af3f-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="6af3f-120">Shader Model 4 (DirectX HLSL) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6af3f-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6af3f-121">Oui</span><span class="sxs-lookup"><span data-stu-id="6af3f-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6af3f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6af3f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af3f-123">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="6af3f-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




