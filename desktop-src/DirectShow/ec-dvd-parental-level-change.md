---
description: Signale que le niveau parental du contenu DVD créé va être modifié.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525421"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="495af-103">\_modification du \_ \_ niveau parental du DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="495af-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="495af-104">Signale que le niveau parental du contenu DVD créé va être modifié.</span><span class="sxs-lookup"><span data-stu-id="495af-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="495af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="495af-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="495af-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="495af-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="495af-107">Valeur de type LONG représentant le nouveau niveau parental défini dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="495af-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="495af-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="495af-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="495af-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="495af-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="495af-110">Notes</span><span class="sxs-lookup"><span data-stu-id="495af-110">Remarks</span></span>

<span data-ttu-id="495af-111">Le filtre de [navigateur DVD](dvd-navigator-filter.md) ne prend pas en charge les modifications de niveau parental pendant la diffusion en continu en réponse aux commandes SetTmpPML sur un disque DVD.</span><span class="sxs-lookup"><span data-stu-id="495af-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="495af-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="495af-112">Requirements</span></span>



| <span data-ttu-id="495af-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="495af-113">Requirement</span></span> | <span data-ttu-id="495af-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="495af-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495af-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="495af-115">Header</span></span><br/> | <dl> <span data-ttu-id="495af-116"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="495af-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495af-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="495af-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495af-118">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="495af-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="495af-119">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="495af-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="495af-120">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="495af-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




