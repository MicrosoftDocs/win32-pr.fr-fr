---
description: Les \_ constantes d’indicateur de bit LINEBUSYMODE décrivent différents signaux occupés que le commutateur ou le réseau peuvent générer. Ces signaux occupés indiquent généralement qu’une ressource différente requise pour effectuer un appel est en cours d’utilisation.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535396"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="9945c-104">\_Constantes LINEBUSYMODE</span><span class="sxs-lookup"><span data-stu-id="9945c-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="9945c-105">Les constantes d’indicateur de bit **LINEBUSYMODE \_** décrivent différents signaux occupés que le commutateur ou le réseau peuvent générer.</span><span class="sxs-lookup"><span data-stu-id="9945c-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="9945c-106">Ces signaux occupés indiquent généralement qu’une ressource différente requise pour effectuer un appel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9945c-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="9945c-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_station LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="9945c-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9945c-108">Le signal occupé indique que la station du tiers appelé est occupée.</span><span class="sxs-lookup"><span data-stu-id="9945c-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="9945c-109">Cela est généralement signalé par un ton occupé *normal* .</span><span class="sxs-lookup"><span data-stu-id="9945c-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9945c-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ Trunk**</span><span class="sxs-lookup"><span data-stu-id="9945c-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9945c-111">Le signal occupé indique qu’un Trunk ou un circuit est occupé.</span><span class="sxs-lookup"><span data-stu-id="9945c-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="9945c-112">Ce nombre est généralement signalé *par une tonalité à forte activité* .</span><span class="sxs-lookup"><span data-stu-id="9945c-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9945c-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="9945c-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9945c-114">Le mode spécifique du signal occupé est actuellement inconnu, mais peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9945c-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9945c-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="9945c-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9945c-116">Le mode spécifique du signal occupé n’est pas disponible et ne sera pas connu.</span><span class="sxs-lookup"><span data-stu-id="9945c-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9945c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9945c-117">Remarks</span></span>

<span data-ttu-id="9945c-118">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9945c-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="9945c-119">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="9945c-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="9945c-120">Les signaux occupés peuvent être envoyés en tant que tonalités inbandes ou messages hors bande.</span><span class="sxs-lookup"><span data-stu-id="9945c-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="9945c-121">L’interface TAPI ne fait aucune hypothèse sur le mécanisme de signalisation spécifique.</span><span class="sxs-lookup"><span data-stu-id="9945c-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9945c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9945c-122">Requirements</span></span>



| <span data-ttu-id="9945c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9945c-123">Requirement</span></span> | <span data-ttu-id="9945c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9945c-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9945c-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9945c-125">TAPI version</span></span><br/> | <span data-ttu-id="9945c-126">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9945c-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9945c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9945c-127">Header</span></span><br/>       | <dl> <span data-ttu-id="9945c-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9945c-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




