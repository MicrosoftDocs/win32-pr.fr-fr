---
title: QuadReadAcrossDiagonal fonction)
description: Retourne la valeur locale spécifiée qui est lue à partir de la voie diagonalement opposée dans ce Quad.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- QuadReadAcrossDiagonal fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991037"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="0efc1-104">QuadReadAcrossDiagonal fonction)</span><span class="sxs-lookup"><span data-stu-id="0efc1-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="0efc1-105">Retourne la valeur locale spécifiée qui est lue à partir de la voie diagonalement opposée dans ce Quad.</span><span class="sxs-lookup"><span data-stu-id="0efc1-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efc1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0efc1-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="0efc1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0efc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0efc1-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="0efc1-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="0efc1-109">Type demandé.</span><span class="sxs-lookup"><span data-stu-id="0efc1-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0efc1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0efc1-110">Return value</span></span>

<span data-ttu-id="0efc1-111">Valeur locale spécifiée qui est lue à partir de la voie diagonalement opposée dans ce Quad.</span><span class="sxs-lookup"><span data-stu-id="0efc1-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efc1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0efc1-112">Remarks</span></span>

<span data-ttu-id="0efc1-113">Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="0efc1-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="0efc1-114">Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.</span><span class="sxs-lookup"><span data-stu-id="0efc1-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="0efc1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0efc1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efc1-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="0efc1-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




