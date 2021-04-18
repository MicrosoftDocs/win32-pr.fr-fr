---
description: Les \_ constantes LINECALLTREATMENT répertorient les traitements pour les appels qui ne sont pas répondus ou en attente. À l’exception de la validation des paramètres de base, le traitement des appels est un passage direct de l’interface TAPI au fournisseur de services.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528997"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="5d815-104">\_Constantes LINECALLTREATMENT</span><span class="sxs-lookup"><span data-stu-id="5d815-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="5d815-105">Les constantes **LINECALLTREATMENT \_** répertorient les traitements pour les appels qui ne sont pas répondus ou en attente.</span><span class="sxs-lookup"><span data-stu-id="5d815-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="5d815-106">À l’exception de la validation des paramètres de base, le traitement des appels est un passage direct de l’interface TAPI au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="5d815-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="5d815-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="5d815-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d815-108">Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend le signal occupé.</span><span class="sxs-lookup"><span data-stu-id="5d815-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d815-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_musique LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="5d815-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d815-110">Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend la musique.</span><span class="sxs-lookup"><span data-stu-id="5d815-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d815-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**\_rappel LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="5d815-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d815-112">Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend un signal de rappel.</span><span class="sxs-lookup"><span data-stu-id="5d815-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d815-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**\_silence LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="5d815-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d815-114">Lorsque l’appel n’est pas activement connecté à un appareil (offre ou onHold), le tiers entend le silence.</span><span class="sxs-lookup"><span data-stu-id="5d815-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d815-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5d815-115">Remarks</span></span>

<span data-ttu-id="5d815-116">La valeur 0x00000000 est réservée pour indiquer que le fournisseur de services ne prend pas en charge les traitements des appels.</span><span class="sxs-lookup"><span data-stu-id="5d815-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="5d815-117">Les valeurs de la plage 0x00000005 à 0x000000FF sont réservées pour une définition ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5d815-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="5d815-118">Les valeurs de la plage 0x00000100 à 0xFFFFFFFF sont réservées à l’attribution par les fournisseurs de services et peuvent inclure l’identification de sélections musicales spécifiques ou d’annonces enregistrées.</span><span class="sxs-lookup"><span data-stu-id="5d815-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d815-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d815-119">Requirements</span></span>



| <span data-ttu-id="5d815-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d815-120">Requirement</span></span> | <span data-ttu-id="5d815-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d815-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d815-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5d815-122">TAPI version</span></span><br/> | <span data-ttu-id="5d815-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5d815-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5d815-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d815-124">Header</span></span><br/>       | <dl> <span data-ttu-id="5d815-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d815-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




