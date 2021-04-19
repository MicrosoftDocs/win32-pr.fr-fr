---
description: Les \_ constantes d’indicateur de bit LINECALLSELECT décrivent les appels à sélectionner.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540070"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="53359-103">\_Constantes LINECALLSELECT</span><span class="sxs-lookup"><span data-stu-id="53359-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="53359-104">Les constantes d’indicateur de bit **LINECALLSELECT \_** décrivent les appels à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="53359-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="53359-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_adresse LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="53359-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="53359-106">Sélectionne l’appel sur l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="53359-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53359-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_appel LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="53359-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="53359-108">Sélectionne les appels associés à l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="53359-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="53359-109">Par exemple, les tiers d’une conférence appellent.</span><span class="sxs-lookup"><span data-stu-id="53359-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53359-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**</span><span class="sxs-lookup"><span data-stu-id="53359-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="53359-111">Sélectionne les appels associés à l’identificateur d’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="53359-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="53359-112">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="53359-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53359-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**</span><span class="sxs-lookup"><span data-stu-id="53359-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="53359-114">Sélectionne des appels sur l’identificateur de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="53359-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="53359-115">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,1 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="53359-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="53359-116">Les applications doivent envisager l’utilisation \_ de la constante de ligne LINECALLSELECT au lieu de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="53359-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="53359-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_ligne LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="53359-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="53359-118">Sélectionne des appels sur le périphérique de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="53359-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53359-119">Notes</span><span class="sxs-lookup"><span data-stu-id="53359-119">Remarks</span></span>

<span data-ttu-id="53359-120">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="53359-120">No extensibility.</span></span> <span data-ttu-id="53359-121">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="53359-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="53359-122">Cette constante est utilisée dans [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) et pour spécifier une sélection (portée) des appels qui sont demandés.</span><span class="sxs-lookup"><span data-stu-id="53359-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="53359-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53359-123">Requirements</span></span>



| <span data-ttu-id="53359-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53359-124">Requirement</span></span> | <span data-ttu-id="53359-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="53359-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="53359-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="53359-126">TAPI version</span></span><br/> | <span data-ttu-id="53359-127">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53359-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="53359-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="53359-128">Header</span></span><br/>       | <dl> <span data-ttu-id="53359-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="53359-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




