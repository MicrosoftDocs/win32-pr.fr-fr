---
description: Signale que l’ensemble de méthodes d’interface IDvdControl2 disponibles a changé.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523559"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="88a67-103">\_ \_ \_ modification UOPs valide du DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="88a67-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="88a67-104">Signale que l’ensemble de méthodes d’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) disponibles a changé.</span><span class="sxs-lookup"><span data-stu-id="88a67-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="88a67-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88a67-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a67-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="88a67-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="88a67-107">Valeur **DWORD** qui contient une combinaison de zéro ou plusieurs indicateurs de l’énumération d' [**\_ \_ indicateur UOP valide**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) .</span><span class="sxs-lookup"><span data-stu-id="88a67-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="88a67-108">Les bits indiquent les commandes [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) qui ont été explicitement désactivées par le disque DVD.</span><span class="sxs-lookup"><span data-stu-id="88a67-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="88a67-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="88a67-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="88a67-110">Zéro.</span><span class="sxs-lookup"><span data-stu-id="88a67-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88a67-111">Notes</span><span class="sxs-lookup"><span data-stu-id="88a67-111">Remarks</span></span>

<span data-ttu-id="88a67-112">Cet événement indique uniquement les opérations qui sont explicitement désactivées par le contenu sur le disque DVD. Cela ne garantit pas qu’il est valide d’appeler des méthodes qui ne sont pas désactivées.</span><span class="sxs-lookup"><span data-stu-id="88a67-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="88a67-113">Par exemple, si aucun bouton n’est présent, la méthode [**IDvdControl2 :: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) ne fonctionnera pas, même si la méthode n’est pas explicitement désactivée.</span><span class="sxs-lookup"><span data-stu-id="88a67-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="88a67-114">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="88a67-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a67-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88a67-115">Requirements</span></span>



| <span data-ttu-id="88a67-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88a67-116">Requirement</span></span> | <span data-ttu-id="88a67-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="88a67-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a67-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="88a67-118">Header</span></span><br/> | <dl> <span data-ttu-id="88a67-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88a67-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88a67-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88a67-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a67-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="88a67-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="88a67-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="88a67-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="88a67-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="88a67-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




