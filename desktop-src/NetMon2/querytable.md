---
description: La structure QUERYTABLE fournit une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: QUERYTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517796"
---
# <a name="querytable-structure"></a><span data-ttu-id="33a17-103">QUERYTABLE, structure</span><span class="sxs-lookup"><span data-stu-id="33a17-103">QUERYTABLE structure</span></span>

<span data-ttu-id="33a17-104">La structure **QUERYTABLE** fournit une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.</span><span class="sxs-lookup"><span data-stu-id="33a17-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33a17-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="33a17-106">Membres</span><span class="sxs-lookup"><span data-stu-id="33a17-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="33a17-107">**nStationQueries**</span><span class="sxs-lookup"><span data-stu-id="33a17-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="33a17-108">En entrée, le nombre maximal d’ordinateurs que vous souhaitez Moniteur réseau renvoyer.</span><span class="sxs-lookup"><span data-stu-id="33a17-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="33a17-109">Lors de la sortie, le nombre de structures [STATIONQUERY](stationquery.md) retournées par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="33a17-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="33a17-110">Chaque structure **STATIONQUERY** représente un ordinateur qui capture actuellement des données.</span><span class="sxs-lookup"><span data-stu-id="33a17-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="33a17-111">**StationQuery**</span><span class="sxs-lookup"><span data-stu-id="33a17-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="33a17-112">En entrée, tableau de structures [STATIONQUERY](stationquery.md) vides qui contient le nombre d’éléments spécifié dans **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="33a17-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="33a17-113">Lors de la sortie, il s’agit d’une structure [STATIONQUERY](stationquery.md) remplie pour chaque ordinateur qui capture des données.</span><span class="sxs-lookup"><span data-stu-id="33a17-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="33a17-114">Le nombre d’éléments remplis est retourné par **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="33a17-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33a17-115">Notes</span><span class="sxs-lookup"><span data-stu-id="33a17-115">Remarks</span></span>

<span data-ttu-id="33a17-116">La mémoire pour cette structure et le tableau [STATIONQUERY](stationquery.md) doit être allouée par l’application appelante et libérée une fois que les informations ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="33a17-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a17-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33a17-117">Requirements</span></span>



| <span data-ttu-id="33a17-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33a17-118">Requirement</span></span> | <span data-ttu-id="33a17-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="33a17-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33a17-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33a17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33a17-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33a17-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="33a17-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33a17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33a17-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33a17-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33a17-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="33a17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a17-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a17-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a17-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33a17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a17-127">IDelaydC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="33a17-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="33a17-128">IESP::QueryStations</span><span class="sxs-lookup"><span data-stu-id="33a17-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="33a17-129">IRTC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="33a17-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="33a17-130">IStats::QueryStations</span><span class="sxs-lookup"><span data-stu-id="33a17-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="33a17-131">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="33a17-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




