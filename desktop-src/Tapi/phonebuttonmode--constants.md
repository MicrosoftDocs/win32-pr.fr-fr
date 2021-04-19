---
description: Les \_ constantes d’indicateur de bit PHONEBUTTONMODE décrivent les classes Button.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Constantes PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535425"
---
# <a name="phonebuttonmode_-constants"></a><span data-ttu-id="b3117-103">\_Constantes PHONEBUTTONMODE</span><span class="sxs-lookup"><span data-stu-id="b3117-103">PHONEBUTTONMODE\_ Constants</span></span>

<span data-ttu-id="b3117-104">Les constantes d’indicateur de bit **PHONEBUTTONMODE \_** décrivent les classes Button.</span><span class="sxs-lookup"><span data-stu-id="b3117-104">The **PHONEBUTTONMODE\_** bit-flag constants describe the button classes.</span></span>

<dl> <dt>

<span data-ttu-id="b3117-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_appel PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="b3117-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-106">Le bouton est assigné à une apparence d’appel.</span><span class="sxs-lookup"><span data-stu-id="b3117-106">The button is assigned to a call appearance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3117-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**\_affichage PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="b3117-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-108">Le bouton est un bouton « Soft » associé à l’affichage du téléphone.</span><span class="sxs-lookup"><span data-stu-id="b3117-108">The button is a "soft" button associated with the phone's display.</span></span> <span data-ttu-id="b3117-109">Un ensemble de téléphones peut avoir zéro ou plusieurs boutons d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b3117-109">A phone set can have zero or more display buttons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3117-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ factice**</span><span class="sxs-lookup"><span data-stu-id="b3117-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE\_DUMMY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-111">Cette valeur est utilisée pour décrire une position de bouton/lampe qui n’a pas de bouton correspondant, mais qui a uniquement un feu.</span><span class="sxs-lookup"><span data-stu-id="b3117-111">This value is used to describe a button/lamp position that has no corresponding button but has only a lamp.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3117-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_fonctionnalité PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="b3117-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**PHONEBUTTONMODE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-113">Le bouton est affecté à la demande de fonctionnalités à partir du commutateur, telles que la suspension, la Conférence et le transfert.</span><span class="sxs-lookup"><span data-stu-id="b3117-113">The button is assigned to requesting features from the switch, such as hold, conference, and transfer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3117-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**\_pavé numérique PHONEBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="b3117-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE\_KEYPAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-115">Le bouton est l’un des douze boutons du clavier, de 0 à 9, de « \* » et de «» \# .</span><span class="sxs-lookup"><span data-stu-id="b3117-115">The button is one of the twelve keypad buttons, 0 through 9, '\*', and '\#'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3117-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ local**</span><span class="sxs-lookup"><span data-stu-id="b3117-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b3117-117">Le bouton est un bouton de fonction local, tel que muet ou contrôle de volume.</span><span class="sxs-lookup"><span data-stu-id="b3117-117">The button is a local function button, such as mute or volume control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3117-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b3117-118">Remarks</span></span>

<span data-ttu-id="b3117-119">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="b3117-119">No extensibility.</span></span> <span data-ttu-id="b3117-120">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="b3117-120">All 32 bits are reserved.</span></span>

<span data-ttu-id="b3117-121">Ce type d’énumération est utilisé dans la structure de données [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) pour décrire la signification associée aux boutons du téléphone.</span><span class="sxs-lookup"><span data-stu-id="b3117-121">This enumeration type is used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to describe the meaning associated with the phone's buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3117-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3117-122">Requirements</span></span>



| <span data-ttu-id="b3117-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3117-123">Requirement</span></span> | <span data-ttu-id="b3117-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3117-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b3117-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b3117-125">TAPI version</span></span><br/> | <span data-ttu-id="b3117-126">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b3117-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b3117-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3117-127">Header</span></span><br/>       | <dl> <span data-ttu-id="b3117-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3117-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




