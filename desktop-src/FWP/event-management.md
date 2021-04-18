---
title: Gestion des événements
description: Gestion des événements
ms.assetid: DA6B76B8-E436-44D0-890D-12EE17960EBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469be4ad7914517b132fbdbafd91ea97f3be482
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314718"
---
# <a name="event-management"></a><span data-ttu-id="8a5e5-103">Gestion des événements</span><span class="sxs-lookup"><span data-stu-id="8a5e5-103">Event Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a5e5-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8a5e5-104">In this section</span></span>

-   [<span data-ttu-id="8a5e5-105">**FWPM \_ net, \_ événement \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-105">**FWPM\_NET\_EVENT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0)
-   [<span data-ttu-id="8a5e5-106">*FWPM \_ net, \_ événement \_ CALLBACK1*</span><span class="sxs-lookup"><span data-stu-id="8a5e5-106">*FWPM\_NET\_EVENT\_CALLBACK1*</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="8a5e5-107">*FWPM \_ net, \_ événement \_ CALLBACK2*</span><span class="sxs-lookup"><span data-stu-id="8a5e5-107">*FWPM\_NET\_EVENT\_CALLBACK2*</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback2)
-   [<span data-ttu-id="8a5e5-108">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-108">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)
-   [<span data-ttu-id="8a5e5-109">**FwpmNetEventDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-109">**FwpmNetEventDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventdestroyenumhandle0)
-   [<span data-ttu-id="8a5e5-110">**FwpmNetEventEnum0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-110">**FwpmNetEventEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)
-   [<span data-ttu-id="8a5e5-111">**FwpmNetEventEnum1**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-111">**FwpmNetEventEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)
-   [<span data-ttu-id="8a5e5-112">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-112">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="8a5e5-113">**FwpmNetEventEnum3**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-113">**FwpmNetEventEnum3**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventenum3)
-   [<span data-ttu-id="8a5e5-114">**FwpmNetEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-114">**FwpmNetEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsgetsecurityinfo0)
-   [<span data-ttu-id="8a5e5-115">**FwpmNetEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-115">**FwpmNetEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventssetsecurityinfo0)
-   [<span data-ttu-id="8a5e5-116">**FwpmNetEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-116">**FwpmNetEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsubscribe0)
-   [<span data-ttu-id="8a5e5-117">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-117">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="8a5e5-118">**FwpmNetEventSubscribe2**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-118">**FwpmNetEventSubscribe2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe2)
-   [<span data-ttu-id="8a5e5-119">**FwpmNetEventSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-119">**FwpmNetEventSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsubscriptionsget0)
-   [<span data-ttu-id="8a5e5-120">**FwpmNetEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="8a5e5-120">**FwpmNetEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventunsubscribe0)

 

 