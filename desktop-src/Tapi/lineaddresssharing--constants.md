---
description: Les \_ constantes d’indicateur de bit LINEADDRESSSHARING décrivent les différentes façons dont une adresse peut être partagée entre les lignes.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541132"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="76771-103">\_Constantes LINEADDRESSSHARING</span><span class="sxs-lookup"><span data-stu-id="76771-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="76771-104">Les constantes d’indicateur de bit **LINEADDRESSSHARING \_** décrivent les différentes façons dont une adresse peut être partagée entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="76771-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="76771-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privé**</span><span class="sxs-lookup"><span data-stu-id="76771-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76771-106">L’adresse est privée pour la ligne de l’utilisateur ; elle n’est attribuée à aucune autre station.</span><span class="sxs-lookup"><span data-stu-id="76771-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76771-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**</span><span class="sxs-lookup"><span data-stu-id="76771-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76771-108">L’adresse est reliée à une ou plusieurs autres stations.</span><span class="sxs-lookup"><span data-stu-id="76771-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="76771-109">La première ligne permettant d’activer un appel sur la ligne aura un accès exclusif à l’adresse et aux appels qui peuvent exister sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="76771-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="76771-110">Les autres lignes ne pourront pas utiliser l’adresse de pont lorsqu’elle est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="76771-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76771-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**</span><span class="sxs-lookup"><span data-stu-id="76771-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76771-112">L’adresse est reliée à une ou plusieurs autres stations.</span><span class="sxs-lookup"><span data-stu-id="76771-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="76771-113">La première ligne pour activer un appel sur la ligne aura uniquement un accès exclusif à l’appel correspondant.</span><span class="sxs-lookup"><span data-stu-id="76771-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="76771-114">Les autres applications qui utilisent l’adresse entraînent des apparences d’appel nouvelles et séparées.</span><span class="sxs-lookup"><span data-stu-id="76771-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76771-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**</span><span class="sxs-lookup"><span data-stu-id="76771-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76771-116">L’adresse est reliée par une ou plusieurs autres lignes.</span><span class="sxs-lookup"><span data-stu-id="76771-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="76771-117">Toutes les parties de pont peuvent partager des appels sur l’adresse, qui fonctionne alors comme une conférence.</span><span class="sxs-lookup"><span data-stu-id="76771-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="76771-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ surveillé**</span><span class="sxs-lookup"><span data-stu-id="76771-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="76771-119">Il s’agit d’une adresse dont l’état inactif/occupé est rendu disponible pour cette ligne.</span><span class="sxs-lookup"><span data-stu-id="76771-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76771-120">Notes</span><span class="sxs-lookup"><span data-stu-id="76771-120">Remarks</span></span>

<span data-ttu-id="76771-121">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="76771-121">No extensibility.</span></span> <span data-ttu-id="76771-122">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="76771-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="76771-123">Le mode de partage d’une adresse entre les lignes peut affecter le comportement de cette adresse.</span><span class="sxs-lookup"><span data-stu-id="76771-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="76771-124">[**Ligne \_**](line-callstate.md) Les messages CALLSTATE et [**line \_ ADDRESSSTATE**](line-addressstate.md) sont envoyés à l’application en réponse aux activités des stations de pontage.</span><span class="sxs-lookup"><span data-stu-id="76771-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="76771-125">Ces messages permettent à une application d’effectuer le suivi de l’état de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="76771-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="76771-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76771-126">Requirements</span></span>



| <span data-ttu-id="76771-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76771-127">Requirement</span></span> | <span data-ttu-id="76771-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="76771-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76771-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="76771-129">TAPI version</span></span><br/> | <span data-ttu-id="76771-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="76771-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="76771-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="76771-131">Header</span></span><br/>       | <dl> <span data-ttu-id="76771-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="76771-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76771-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76771-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76771-134">**ADDRESSSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="76771-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="76771-135">**CALLSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="76771-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




