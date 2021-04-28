---
description: 'WorldToObject4x3 : matrice de transformation de l’espace universel vers l’espace de l’objet.'
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105246"
---
# <a name="worldtoobject4x3"></a><span data-ttu-id="83474-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="83474-103">WorldToObject4x3</span></span>

<span data-ttu-id="83474-104">Matrice pour la transformation de l’espace universel à l’espace de l’objet.</span><span class="sxs-lookup"><span data-stu-id="83474-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="83474-105">Object-Space fait référence à l’espace de la structure d’accélération de niveau inférieur actuelle.</span><span class="sxs-lookup"><span data-stu-id="83474-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="83474-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83474-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="83474-107">Notes </span><span class="sxs-lookup"><span data-stu-id="83474-107">Remarks</span></span>

<span data-ttu-id="83474-108">La matrice est une transposition de la matrice **WorldToObject3x4** .</span><span class="sxs-lookup"><span data-stu-id="83474-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="83474-109">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="83474-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="83474-110">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="83474-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="83474-111">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="83474-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="83474-112">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="83474-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="83474-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83474-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83474-114">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="83474-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




