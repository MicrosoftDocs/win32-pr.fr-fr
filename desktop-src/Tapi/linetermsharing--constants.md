---
description: Les \_ constantes d’indicateur de bit LINETERMSHARING décrivent les différentes façons dont un terminal peut être partagé entre des appareils de ligne, des adresses ou des appels.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537454"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="6c737-103">\_Constantes LINETERMSHARING</span><span class="sxs-lookup"><span data-stu-id="6c737-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="6c737-104">Les constantes d’indicateur de bit **LINETERMSHARING \_** décrivent les différentes façons dont un terminal peut être partagé entre des appareils de ligne, des adresses ou des appels.</span><span class="sxs-lookup"><span data-stu-id="6c737-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="6c737-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privé**</span><span class="sxs-lookup"><span data-stu-id="6c737-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c737-106">L’appareil terminal est privé sur un appareil à ligne unique.</span><span class="sxs-lookup"><span data-stu-id="6c737-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c737-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**</span><span class="sxs-lookup"><span data-stu-id="6c737-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c737-108">Le périphérique terminal peut être utilisé par plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="6c737-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="6c737-109">Les requêtes [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) des différents terminaux finissent par être fusionnées ou interrogées sur le terminal.</span><span class="sxs-lookup"><span data-stu-id="6c737-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c737-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**</span><span class="sxs-lookup"><span data-stu-id="6c737-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c737-111">Le périphérique terminal peut être utilisé par plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="6c737-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="6c737-112">Le dernier périphérique de ligne à faire un [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ou un [**\_ lineSetTerminal TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) sur le terminal pour un mode terminal donné disposera d’une connexion exclusive au terminal pour ce mode.</span><span class="sxs-lookup"><span data-stu-id="6c737-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c737-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6c737-113">Remarks</span></span>

<span data-ttu-id="6c737-114">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="6c737-114">No extensibility.</span></span> <span data-ttu-id="6c737-115">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="6c737-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="6c737-116">Ces constantes décrivent les classes de flux de contrôle et d’informations qui peuvent être acheminées directement entre un appareil de ligne et un périphérique terminal (tel qu’un ensemble de téléphones).</span><span class="sxs-lookup"><span data-stu-id="6c737-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c737-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c737-117">Requirements</span></span>



| <span data-ttu-id="6c737-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c737-118">Requirement</span></span> | <span data-ttu-id="6c737-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c737-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c737-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6c737-120">TAPI version</span></span><br/> | <span data-ttu-id="6c737-121">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6c737-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6c737-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c737-122">Header</span></span><br/>       | <dl> <span data-ttu-id="6c737-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c737-123"><dt>Tapi.h</dt></span></span> </dl> |



 

