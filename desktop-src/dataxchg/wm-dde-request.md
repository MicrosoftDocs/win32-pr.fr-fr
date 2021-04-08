---
title: Message WM_DDE_REQUEST (DDE. h)
description: Une application cliente de échange dynamique de données (DDE) envoie un \_ message de requête de l’échange de données (DDE) WM \_ à une application de serveur DDE pour demander la valeur d’un élément de données. Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741085"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="4cdb4-105">\_Message de \_ requête DDE WM</span><span class="sxs-lookup"><span data-stu-id="4cdb4-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="4cdb4-106">Une application cliente de échange dynamique de données (DDE) envoie un message de **\_ \_ requête** de l’échange de données (DDE) WM à une application de serveur DDE pour demander la valeur d’un élément de données.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="4cdb4-107">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="4cdb4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cdb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdb4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cdb4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdb4-110">Handle de la fenêtre cliente qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="4cdb4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cdb4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdb4-112">Le mot de poids faible spécifie un format de presse-papiers standard ou inscrit.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="4cdb4-113">Le mot de poids fort contient un atome qui identifie l’élément de données demandé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cdb4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4cdb4-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="4cdb4-115">Publication</span><span class="sxs-lookup"><span data-stu-id="4cdb4-115">Posting</span></span>

<span data-ttu-id="4cdb4-116">L’application cliente alloue Atom en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="4cdb4-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="4cdb4-117">Réception</span><span class="sxs-lookup"><span data-stu-id="4cdb4-117">Receiving</span></span>

<span data-ttu-id="4cdb4-118">Si l’application de réception (serveur) peut répondre à la demande, elle répond avec un message de [**\_ \_ données de l’échange WM**](wm-dde-data.md) contenant les données demandées.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="4cdb4-119">Dans le cas contraire, il répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="4cdb4-120">Lorsque vous répondez avec un message de type de [**\_ \_ données DDE**](wm-dde-data.md) ou un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM, l’application serveur peut réutiliser l’Atom ou supprimer l’atome et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdb4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cdb4-121">Requirements</span></span>



| <span data-ttu-id="4cdb4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cdb4-122">Requirement</span></span> | <span data-ttu-id="4cdb4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cdb4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdb4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cdb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4cdb4-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cdb4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4cdb4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cdb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4cdb4-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cdb4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4cdb4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cdb4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cdb4-129"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cdb4-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cdb4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cdb4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="4cdb4-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4cdb4-132">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="4cdb4-133">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="4cdb4-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="4cdb4-135">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="4cdb4-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="4cdb4-137">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="4cdb4-138">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="4cdb4-139">**\_données DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="4cdb4-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4cdb4-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4cdb4-141">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="4cdb4-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

