---
description: Utilisé dans un nuanceur de correspondance pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon.
ms.assetid: ''
title: Fonction AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513938"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="ea04f-103">Fonction AcceptHitAndEndSearch</span><span class="sxs-lookup"><span data-stu-id="ea04f-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="ea04f-104">Utilisé dans un [nuanceur de correspondance](any-hit-shader.md) pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon.</span><span class="sxs-lookup"><span data-stu-id="ea04f-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="ea04f-105">Si un nuanceur d’intersection est en cours d’exécution, son exécution s’arrête.</span><span class="sxs-lookup"><span data-stu-id="ea04f-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="ea04f-106">L’exécution passe au [nuanceur de correspondance le plus proche](closest-hit-shader.md), s’il est activé, avec l’accès le plus proche jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="ea04f-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea04f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea04f-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="ea04f-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ea04f-108">Return Value</span></span>

<span data-ttu-id="ea04f-109">**void**</span><span class="sxs-lookup"><span data-stu-id="ea04f-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="ea04f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ea04f-110">Remarks</span></span>

<span data-ttu-id="ea04f-111">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="ea04f-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="ea04f-112">**Nuanceur pouvant être appelé**</span><span class="sxs-lookup"><span data-stu-id="ea04f-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="ea04f-113">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="ea04f-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="ea04f-114">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="ea04f-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="ea04f-115">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="ea04f-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="ea04f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea04f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea04f-117">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="ea04f-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




