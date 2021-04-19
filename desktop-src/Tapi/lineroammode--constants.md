---
description: Les \_ constantes d’indicateur de bit LINEROAMMODE décrivent l’état d’itinérance d’un périphérique de ligne.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Constantes LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530475"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="45c27-103">\_Constantes LINEROAMMODE</span><span class="sxs-lookup"><span data-stu-id="45c27-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="45c27-104">Les constantes d’indicateur de bit **LINEROAMMODE \_** décrivent l’état d’itinérance d’un périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="45c27-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="45c27-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**Page d’LINEROAMMODE \_**</span><span class="sxs-lookup"><span data-stu-id="45c27-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45c27-106">La ligne est connectée au nœud réseau d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="45c27-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45c27-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE \_ itinéranta**</span><span class="sxs-lookup"><span data-stu-id="45c27-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45c27-108">La ligne est connectée à l’itinérance : un opérateur et les appels sont facturés en conséquence.</span><span class="sxs-lookup"><span data-stu-id="45c27-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45c27-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE \_ ROAMB**</span><span class="sxs-lookup"><span data-stu-id="45c27-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45c27-110">La ligne est connectée au transporteur itinérant-B et les appels sont facturés en conséquence.</span><span class="sxs-lookup"><span data-stu-id="45c27-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45c27-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="45c27-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45c27-112">Le mode itinérant n’est pas disponible et ne sera pas connu.</span><span class="sxs-lookup"><span data-stu-id="45c27-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45c27-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="45c27-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45c27-114">Le mode itinérant est actuellement inconnu, mais peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="45c27-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45c27-115">Notes</span><span class="sxs-lookup"><span data-stu-id="45c27-115">Remarks</span></span>

<span data-ttu-id="45c27-116">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="45c27-116">No extensibility.</span></span> <span data-ttu-id="45c27-117">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="45c27-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c27-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45c27-118">Requirements</span></span>



| <span data-ttu-id="45c27-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45c27-119">Requirement</span></span> | <span data-ttu-id="45c27-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="45c27-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="45c27-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="45c27-121">TAPI version</span></span><br/> | <span data-ttu-id="45c27-122">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="45c27-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="45c27-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="45c27-123">Header</span></span><br/>       | <dl> <span data-ttu-id="45c27-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c27-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




