---
description: Appelée à partir d’un nuanceur d’accès quelconque pour rejeter l’accès et terminer le nuanceur.
ms.assetid: ''
title: Fonction IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516393"
---
# <a name="ignorehit-function"></a><span data-ttu-id="2144e-103">Fonction IgnoreHit</span><span class="sxs-lookup"><span data-stu-id="2144e-103">IgnoreHit function</span></span>

<span data-ttu-id="2144e-104">Appelée à partir d’un [nuanceur d’accès quelconque](any-hit-shader.md) pour rejeter l’accès et terminer le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2144e-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="2144e-105">La recherche d’accès se poursuit sans valider la distance et les attributs pour l’accès actuel.</span><span class="sxs-lookup"><span data-stu-id="2144e-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="2144e-106">L’appel [**ReportHit**](reporthit-function.md) dans le [nuanceur d’intersection](intersection-shader.md), le cas échéant, retourne la valeur false.</span><span class="sxs-lookup"><span data-stu-id="2144e-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="2144e-107">Toutes les modifications apportées à la charge utile de rayon jusqu’à ce point dans le nuanceur d’accès sont conservées.</span><span class="sxs-lookup"><span data-stu-id="2144e-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="2144e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2144e-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="2144e-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2144e-109">Return Value</span></span>

<span data-ttu-id="2144e-110">**void**</span><span class="sxs-lookup"><span data-stu-id="2144e-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="2144e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2144e-111">Remarks</span></span>

<span data-ttu-id="2144e-112">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="2144e-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="2144e-113">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="2144e-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="2144e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2144e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2144e-115">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="2144e-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




