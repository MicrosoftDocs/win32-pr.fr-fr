---
description: Appelé par un nuanceur d’intersection pour signaler une intersection de rayon.
ms.assetid: ''
title: Fonction ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515171"
---
# <a name="reporthit-function"></a><span data-ttu-id="aaa22-103">Fonction ReportHit</span><span class="sxs-lookup"><span data-stu-id="aaa22-103">ReportHit function</span></span>

<span data-ttu-id="aaa22-104">Appelé par un [nuanceur d’intersection](intersection-shader.md) pour signaler une intersection de rayon.</span><span class="sxs-lookup"><span data-stu-id="aaa22-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa22-105">Syntax</span></span>
<span data-ttu-id="aaa22-106">Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :</span><span class="sxs-lookup"><span data-stu-id="aaa22-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="aaa22-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaa22-107">Parameters</span></span>

`THit`

<span data-ttu-id="aaa22-108">Valeur float spécifiant la distance paramétrique de l’intersection.</span><span class="sxs-lookup"><span data-stu-id="aaa22-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="aaa22-109">Entier non signé qui identifie le type d’accès qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="aaa22-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="aaa22-110">Il s’agit d’une valeur spécifiée par l’utilisateur dans la plage 0-127.</span><span class="sxs-lookup"><span data-stu-id="aaa22-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="aaa22-111">La valeur peut être lue par [n’importe quel](any-hit-shader.md) nuanceur de correspondance ou d' [accès le plus proche](closest-hit-shader.md) avec l’intrinsèque **HitKind** .</span><span class="sxs-lookup"><span data-stu-id="aaa22-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="aaa22-112">Structure de structure d' [**attribut d’intersection**](intersection-attributes.md) définie par l’utilisateur qui spécifie les attributs d’intersection.</span><span class="sxs-lookup"><span data-stu-id="aaa22-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="aaa22-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aaa22-113">Return Value</span></span>

<span data-ttu-id="aaa22-114">valeur **booléenne** True si l’accès a été accepté.</span><span class="sxs-lookup"><span data-stu-id="aaa22-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="aaa22-115">Un accès est rejeté si *cela* est en dehors de l’intervalle de rayon actuel, ou si le nuanceur de correspondance n’appelle [**IgnoreHit**](ignorehit-function.md).</span><span class="sxs-lookup"><span data-stu-id="aaa22-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="aaa22-116">L’intervalle de rayon actuel est défini par **RayTMin** et **RayTCurrent**.</span><span class="sxs-lookup"><span data-stu-id="aaa22-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa22-117">Notes</span><span class="sxs-lookup"><span data-stu-id="aaa22-117">Remarks</span></span>

<span data-ttu-id="aaa22-118">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="aaa22-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="aaa22-119">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="aaa22-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="aaa22-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa22-121">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="aaa22-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




