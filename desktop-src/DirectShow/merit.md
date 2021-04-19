---
description: Les valeurs mérite définissent l’ordre dans lequel le gestionnaire de graphes de filtre tente d’ajouter des filtres lors de la génération du graphique.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérite (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535222"
---
# <a name="merit"></a><span data-ttu-id="32ea8-103">Mérite</span><span class="sxs-lookup"><span data-stu-id="32ea8-103">Merit</span></span>

<span data-ttu-id="32ea8-104">Les valeurs mérite définissent l’ordre dans lequel le gestionnaire de graphes de filtre tente d’ajouter des filtres lors de la génération du graphique.</span><span class="sxs-lookup"><span data-stu-id="32ea8-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="32ea8-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérite \_ Préféré** (0x800000) mérite <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ normal** (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **mérite \_ improbable** (0x400000) mériter <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ n' \_ \_ utiliser pas** (0x200000) le compresseur de <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ SW \_** () <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** mérite le compresseur de matériel (0x100050)</span><span class="sxs-lookup"><span data-stu-id="32ea8-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="32ea8-106">Notes</span><span class="sxs-lookup"><span data-stu-id="32ea8-106">Remarks</span></span>

<span data-ttu-id="32ea8-107">Chaque filtre est inscrit avec une valeur mérite.</span><span class="sxs-lookup"><span data-stu-id="32ea8-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="32ea8-108">Lorsque le gestionnaire de graphique de filtre crée un graphique, il énumère tous les filtres inscrits avec le type de média correct.</span><span class="sxs-lookup"><span data-stu-id="32ea8-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="32ea8-109">Il les essaie ensuite dans l’ordre de leur mérite, du plus élevé au plus bas.</span><span class="sxs-lookup"><span data-stu-id="32ea8-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="32ea8-110">(Il utilise des critères supplémentaires pour choisir entre les filtres avec des mérites identiques.) Il ne tente jamais de filtrer avec une valeur mérite inférieure ou égale à la valeur **mérite \_ do \_ not \_ use**.</span><span class="sxs-lookup"><span data-stu-id="32ea8-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="32ea8-111">Un filtre qui ne doit jamais être pris en compte pour une lecture ordinaire doit avoir un mérite de **mérite \_ n' \_ \_ utilise pas au** maximum.</span><span class="sxs-lookup"><span data-stu-id="32ea8-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="32ea8-112">Les filtres peuvent être enregistrés avec des valeurs intermédiaires non définies par cette énumération, telles que **mérite \_ normal** + 1.</span><span class="sxs-lookup"><span data-stu-id="32ea8-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ea8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32ea8-113">Requirements</span></span>



| <span data-ttu-id="32ea8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32ea8-114">Requirement</span></span> | <span data-ttu-id="32ea8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="32ea8-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32ea8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="32ea8-116">Header</span></span><br/> | <dl> <span data-ttu-id="32ea8-117"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ea8-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ea8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32ea8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ea8-119">Constantes et GUID</span><span class="sxs-lookup"><span data-stu-id="32ea8-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="32ea8-120">Instructions pour l’enregistrement des filtres</span><span class="sxs-lookup"><span data-stu-id="32ea8-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="32ea8-121">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="32ea8-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




