---
description: Matrice pour la transformation de l’espace objet en espace universel.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 04f80dde64984010c6e015f6e885565396d3b9c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516175"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="6b154-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="6b154-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="6b154-104">Matrice pour la transformation de l’espace objet en espace universel.</span><span class="sxs-lookup"><span data-stu-id="6b154-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="6b154-105">Object-Space fait référence à l’espace de la structure d’accélération de niveau inférieur actuelle.</span><span class="sxs-lookup"><span data-stu-id="6b154-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b154-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b154-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="6b154-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6b154-107">Remarks</span></span>

<span data-ttu-id="6b154-108">La matrice est une transposition de la matrice **ObjectToWorld4x3** .</span><span class="sxs-lookup"><span data-stu-id="6b154-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="6b154-109">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="6b154-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="6b154-110">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="6b154-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="6b154-111">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="6b154-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="6b154-112">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="6b154-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="6b154-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b154-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b154-114">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="6b154-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




