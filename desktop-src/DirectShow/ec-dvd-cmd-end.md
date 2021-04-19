---
description: Signale qu’une commande de navigateur de DVD particulière est terminée.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542223"
---
# <a name="ec_dvd_cmd_end"></a><span data-ttu-id="2f19b-103">fin de la commande de DVD de la EC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f19b-103">EC\_DVD\_CMD\_END</span></span>

<span data-ttu-id="2f19b-104">Signale qu’une commande de [navigateur de DVD](dvd-navigator-filter.md) particulière est terminée.</span><span class="sxs-lookup"><span data-stu-id="2f19b-104">Signals that a particular [DVD Navigator](dvd-navigator-filter.md) command has completed.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f19b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f19b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f19b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2f19b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2f19b-107">Identificateur de commande.</span><span class="sxs-lookup"><span data-stu-id="2f19b-107">Command identifier.</span></span> <span data-ttu-id="2f19b-108">Transmettez ce paramètre à la méthode [**IDvdInfo2 :: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) pour récupérer un pointeur d’interface [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="2f19b-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="2f19b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2f19b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2f19b-110">Valeur **HRESULT** qui indique l’état de la commande.</span><span class="sxs-lookup"><span data-stu-id="2f19b-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f19b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2f19b-111">Remarks</span></span>

<span data-ttu-id="2f19b-112">Cet événement est déclenché uniquement si votre application définit l’indicateur \_ \_ \_ SendEvents de l’indicateur de commande de DVD dans une méthode [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) qui prend un indicateur d' [**\_ \_ indicateurs de cmd DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="2f19b-112">This event is only fired if your application sets the DVD\_CMD\_FLAG\_SendEvents flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="2f19b-113">Cet événement est déclenché dans le domaine de titre.</span><span class="sxs-lookup"><span data-stu-id="2f19b-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f19b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f19b-114">Requirements</span></span>



| <span data-ttu-id="2f19b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f19b-115">Requirement</span></span> | <span data-ttu-id="2f19b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f19b-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f19b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f19b-117">Header</span></span><br/> | <dl> <span data-ttu-id="2f19b-118"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f19b-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f19b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f19b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f19b-120">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="2f19b-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2f19b-121">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="2f19b-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2f19b-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="2f19b-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="2f19b-123">Synchronisation des commandes de DVD</span><span class="sxs-lookup"><span data-stu-id="2f19b-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




