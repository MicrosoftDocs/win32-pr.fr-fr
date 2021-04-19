---
description: Les \_ constantes d’indicateur de bit LINECALLCOMPLMODE décrivent les différentes façons dont un appel peut être effectué.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528491"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="86b0c-103">\_Constantes LINECALLCOMPLMODE</span><span class="sxs-lookup"><span data-stu-id="86b0c-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="86b0c-104">Les constantes d’indicateur de bit **LINECALLCOMPLMODE \_** décrivent les différentes façons dont un appel peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="86b0c-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="86b0c-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_rappel LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="86b0c-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="86b0c-106">Demande à la station appelée de retourner l’appel lorsqu’elle retourne à inactif.</span><span class="sxs-lookup"><span data-stu-id="86b0c-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="86b0c-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**</span><span class="sxs-lookup"><span data-stu-id="86b0c-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="86b0c-108">Met l’appel en file d’attente jusqu’à ce que l’appel puisse être effectué.</span><span class="sxs-lookup"><span data-stu-id="86b0c-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="86b0c-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrus**</span><span class="sxs-lookup"><span data-stu-id="86b0c-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="86b0c-110">Ajoute l’application à l’appel existant à la station appelée (chaland dans).</span><span class="sxs-lookup"><span data-stu-id="86b0c-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="86b0c-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_message LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="86b0c-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="86b0c-112">Conserve un bref message prédéfini pour la station appelée (laisser le mot appelé).</span><span class="sxs-lookup"><span data-stu-id="86b0c-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="86b0c-113">Le message à envoyer est spécifié séparément.</span><span class="sxs-lookup"><span data-stu-id="86b0c-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86b0c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="86b0c-114">Remarks</span></span>

<span data-ttu-id="86b0c-115">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="86b0c-115">No extensibility.</span></span> <span data-ttu-id="86b0c-116">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="86b0c-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b0c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86b0c-117">Requirements</span></span>



| <span data-ttu-id="86b0c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86b0c-118">Requirement</span></span> | <span data-ttu-id="86b0c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="86b0c-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="86b0c-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="86b0c-120">TAPI version</span></span><br/> | <span data-ttu-id="86b0c-121">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="86b0c-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="86b0c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="86b0c-122">Header</span></span><br/>       | <dl> <span data-ttu-id="86b0c-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b0c-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




