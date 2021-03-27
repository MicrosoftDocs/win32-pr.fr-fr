---
title: maxtessfactor
description: Indique la valeur maximale que le nuanceur de coque retourne pour tout facteur de pavage.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841678"
---
# <a name="maxtessfactor"></a><span data-ttu-id="8d28b-103">maxtessfactor</span><span class="sxs-lookup"><span data-stu-id="8d28b-103">maxtessfactor</span></span>

<span data-ttu-id="8d28b-104">Indique la valeur maximale que le nuanceur de coque retourne pour tout facteur de pavage.</span><span class="sxs-lookup"><span data-stu-id="8d28b-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="8d28b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8d28b-105">Remarks</span></span>

<span data-ttu-id="8d28b-106">Cet attribut place une limite supérieure sur la quantité de pavage demandée pour aider un pilote à déterminer la quantité maximale de ressources requises pour le pavage.</span><span class="sxs-lookup"><span data-stu-id="8d28b-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="8d28b-107">Cet attribut est pris en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8d28b-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8d28b-108">Sommet</span><span class="sxs-lookup"><span data-stu-id="8d28b-108">Vertex</span></span> | <span data-ttu-id="8d28b-109">Forme</span><span class="sxs-lookup"><span data-stu-id="8d28b-109">Hull</span></span> | <span data-ttu-id="8d28b-110">Domain</span><span class="sxs-lookup"><span data-stu-id="8d28b-110">Domain</span></span> | <span data-ttu-id="8d28b-111">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8d28b-111">Geometry</span></span> | <span data-ttu-id="8d28b-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="8d28b-112">Pixel</span></span> | <span data-ttu-id="8d28b-113">Compute</span><span class="sxs-lookup"><span data-stu-id="8d28b-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="8d28b-114">x</span><span class="sxs-lookup"><span data-stu-id="8d28b-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="8d28b-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d28b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d28b-116">Attributs du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="8d28b-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="8d28b-117">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8d28b-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




