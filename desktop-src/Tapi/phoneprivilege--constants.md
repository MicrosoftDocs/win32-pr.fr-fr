---
description: Les \_ constantes d’indicateur de bit PHONEPRIVILEGE décrivent les différentes façons d’ouvrir un appareil téléphonique.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526706"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="2f3c8-103">\_Constantes PHONEPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="2f3c8-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="2f3c8-104">Les constantes d’indicateur de bit **PHONEPRIVILEGE \_** décrivent les différentes façons d’ouvrir un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="2f3c8-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**\_moniteur PHONEPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="2f3c8-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2f3c8-106">Une application qui ouvre un appareil téléphonique avec le privilège moniteur est informée des événements et des modifications d’État sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="2f3c8-107">L’application ne peut pas appeler les opérations sur le périphérique téléphonique qui modifieraient son état, de sorte que seules les opérations d’État peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="2f3c8-108">Plusieurs applications peuvent surveiller un appareil téléphonique à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f3c8-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**\_propriétaire PHONEPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="2f3c8-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2f3c8-110">Une application qui ouvre un appareil téléphonique avec le privilège propriétaire est autorisée à modifier l’état des lampes, de la sonnerie, de l’affichage, du hookswitch et des blocs de données du téléphone.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="2f3c8-111">L’ouverture d’un appareil téléphonique en mode propriétaire permet également d’analyser l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="2f3c8-112">Une seule application est autorisée à être le propriétaire d’un appareil téléphonique à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f3c8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2f3c8-113">Remarks</span></span>

<span data-ttu-id="2f3c8-114">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-114">No extensibility.</span></span> <span data-ttu-id="2f3c8-115">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="2f3c8-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3c8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f3c8-116">Requirements</span></span>



| <span data-ttu-id="2f3c8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f3c8-117">Requirement</span></span> | <span data-ttu-id="2f3c8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f3c8-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c8-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2f3c8-119">TAPI version</span></span><br/> | <span data-ttu-id="2f3c8-120">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2f3c8-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2f3c8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f3c8-121">Header</span></span><br/>       | <dl> <span data-ttu-id="2f3c8-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c8-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




