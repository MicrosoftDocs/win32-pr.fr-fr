---
title: Message WM_DDE_UNADVISE (DDE. h)
description: Une application cliente de échange dynamique de données (DDE) publie \_ un \_ message de notification d’inversion DDE WM pour informer une application serveur DDE que l’élément spécifié ou un format de presse-papiers particulier pour l’élément ne doit plus être mis à jour.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466367"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="b56f6-104">\_Message d' \_ innotification DDE</span><span class="sxs-lookup"><span data-stu-id="b56f6-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="b56f6-105">Une application cliente de échange dynamique de données (DDE) publie un message de **\_ \_ notification** d’inversion DDE WM pour informer une application serveur DDE que l’élément spécifié ou un format de presse-papiers particulier pour l’élément ne doit plus être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b56f6-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="b56f6-106">Cela met fin au lien de données chaud ou chaud pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="b56f6-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="b56f6-107">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b56f6-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="b56f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b56f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56f6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b56f6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b56f6-110">Handle de la fenêtre cliente qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="b56f6-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="b56f6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b56f6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b56f6-112">Le mot de poids faible spécifie le format du presse-papiers de l’élément pour lequel la demande de mise à jour est retirée.</span><span class="sxs-lookup"><span data-stu-id="b56f6-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="b56f6-113">Si la **valeur est null**, toutes les conversations de [**\_ \_ notifications WM DDE**](wm-dde-advise.md) actives pour l’élément doivent être arrêtées.</span><span class="sxs-lookup"><span data-stu-id="b56f6-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="b56f6-114">Le mot de poids fort contient un atome global qui identifie l’élément pour lequel la demande de mise à jour est retirée.</span><span class="sxs-lookup"><span data-stu-id="b56f6-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="b56f6-115">Si la **valeur est null**, tous les liens de [**\_ \_ notification WM DDE**](wm-dde-advise.md) actifs associés à la conversation doivent être terminés.</span><span class="sxs-lookup"><span data-stu-id="b56f6-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b56f6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b56f6-116">Remarks</span></span>

<span data-ttu-id="b56f6-117">L’application cliente alloue le mot de poids fort de *lParam* en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="b56f6-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="b56f6-118">L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement.</span><span class="sxs-lookup"><span data-stu-id="b56f6-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="b56f6-119">Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le serveur peut réutiliser l’Atom, ou il peut supprimer l’atome et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="b56f6-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="b56f6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b56f6-120">Requirements</span></span>



| <span data-ttu-id="b56f6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b56f6-121">Requirement</span></span> | <span data-ttu-id="b56f6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b56f6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56f6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b56f6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b56f6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b56f6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b56f6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b56f6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b56f6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b56f6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b56f6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b56f6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b56f6-128"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b56f6-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56f6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b56f6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b56f6-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b56f6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b56f6-131">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="b56f6-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="b56f6-132">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b56f6-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="b56f6-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="b56f6-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="b56f6-134">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b56f6-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="b56f6-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="b56f6-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="b56f6-136">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b56f6-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="b56f6-137">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="b56f6-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="b56f6-138">**\_avis DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="b56f6-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="b56f6-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b56f6-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b56f6-140">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="b56f6-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

