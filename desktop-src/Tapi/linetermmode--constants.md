---
description: Les \_ constantes d’indicateur de bit LINETERMMODE décrivent les différents types d’événements sur une ligne téléphonique qui peuvent être routés vers un appareil terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528077"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="c0b98-103">\_Constantes LINETERMMODE</span><span class="sxs-lookup"><span data-stu-id="c0b98-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="c0b98-104">Les constantes d’indicateur de bit **LINETERMMODE \_** décrivent les différents types d’événements sur une ligne téléphonique qui peuvent être routés vers un appareil terminal.</span><span class="sxs-lookup"><span data-stu-id="c0b98-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="c0b98-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_boutons LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-106">Il s’agit d’événements bouton-pression envoyés du terminal à la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0b98-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**\_affichage LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-108">Il s’agit des informations d’affichage envoyées à partir de la ligne vers le terminal.</span><span class="sxs-lookup"><span data-stu-id="c0b98-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="c0b98-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-110">Il s’agit des événements hookswitch envoyés du terminal à la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0b98-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lampes LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-112">Il s’agit d’événements de lampe envoyés de la ligne vers le terminal.</span><span class="sxs-lookup"><span data-stu-id="c0b98-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="c0b98-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-114">Il s’agit du flux de média bidirectionnel associé à un appel sur la ligne et le terminal.</span><span class="sxs-lookup"><span data-stu-id="c0b98-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="c0b98-115">Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel ne peut pas être contrôlé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="c0b98-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-117">Il s’agit du flux de média unidirectionnel de la ligne vers le terminal associé à un appel sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0b98-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="c0b98-118">Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel peut être contrôlé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="c0b98-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-120">Il s’agit du flux de média unidirectionnel entre le terminal et la ligne associée à un appel sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="c0b98-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="c0b98-121">Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel peut être contrôlé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="c0b98-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c0b98-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_sonnerie LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="c0b98-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c0b98-123">Il s’agit des informations de contrôle de sonnerie envoyées du commutateur au terminal.</span><span class="sxs-lookup"><span data-stu-id="c0b98-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0b98-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c0b98-124">Remarks</span></span>

<span data-ttu-id="c0b98-125">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="c0b98-125">No extensibility.</span></span> <span data-ttu-id="c0b98-126">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="c0b98-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="c0b98-127">Ces constantes décrivent les classes de flux de contrôle et d’informations qui peuvent être acheminées directement entre un appareil de ligne et un périphérique terminal (tel qu’un ensemble de téléphones).</span><span class="sxs-lookup"><span data-stu-id="c0b98-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b98-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b98-128">Requirements</span></span>



| <span data-ttu-id="c0b98-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0b98-129">Requirement</span></span> | <span data-ttu-id="c0b98-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b98-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c0b98-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c0b98-131">TAPI version</span></span><br/> | <span data-ttu-id="c0b98-132">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c0b98-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c0b98-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0b98-133">Header</span></span><br/>       | <dl> <span data-ttu-id="c0b98-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b98-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 




