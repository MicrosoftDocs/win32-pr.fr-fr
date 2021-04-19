---
description: Retourne la valeur passée comme paramètre HitKind à ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529097"
---
# <a name="hitkind"></a><span data-ttu-id="ec42a-103">HitKind</span><span class="sxs-lookup"><span data-stu-id="ec42a-103">HitKind</span></span>

<span data-ttu-id="ec42a-104">Retourne la valeur passée comme paramètre **HitKind** à [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec42a-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec42a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec42a-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="ec42a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ec42a-106">Remarks</span></span>

<span data-ttu-id="ec42a-107">Si l’intersection a été signalée par une intersection de triangle à fonction fixe, **HitKind** sera l’une des faces **\_ \_ \_ avant \_** du triangle du type d’accès (254) ou le type de point d’accès (255). **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec42a-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="ec42a-108">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="ec42a-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="ec42a-109">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="ec42a-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="ec42a-110">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="ec42a-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="ec42a-111">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="ec42a-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="ec42a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec42a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec42a-113">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="ec42a-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




