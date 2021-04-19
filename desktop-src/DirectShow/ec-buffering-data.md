---
description: Le graphique met en mémoire tampon des données ou a arrêté la mise en mémoire tampon des données.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532226"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="edebf-103">\_données de mise en mémoire tampon EC \_</span><span class="sxs-lookup"><span data-stu-id="edebf-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="edebf-104">Le graphique met en mémoire tampon des données ou a arrêté la mise en mémoire tampon des données.</span><span class="sxs-lookup"><span data-stu-id="edebf-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="edebf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edebf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edebf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="edebf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="edebf-107">(**Bool**) **True** si le graphique commence à être mis en mémoire tampon, ou **false** si le graphique a cessé de mettre en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="edebf-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="edebf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="edebf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="edebf-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="edebf-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="edebf-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="edebf-110">Default Action</span></span>

<span data-ttu-id="edebf-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="edebf-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="edebf-112">Notes</span><span class="sxs-lookup"><span data-stu-id="edebf-112">Remarks</span></span>

<span data-ttu-id="edebf-113">Un filtre peut envoyer cet événement s’il doit mettre en mémoire tampon des données à partir d’une source externe.</span><span class="sxs-lookup"><span data-stu-id="edebf-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="edebf-114">(Par exemple, il peut charger des données à partir d’un réseau.) L’application peut utiliser cet événement pour ajuster son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="edebf-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="edebf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edebf-115">Requirements</span></span>



| <span data-ttu-id="edebf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edebf-116">Requirement</span></span> | <span data-ttu-id="edebf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="edebf-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edebf-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="edebf-118">Header</span></span><br/> | <dl> <span data-ttu-id="edebf-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="edebf-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edebf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edebf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edebf-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="edebf-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="edebf-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="edebf-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




