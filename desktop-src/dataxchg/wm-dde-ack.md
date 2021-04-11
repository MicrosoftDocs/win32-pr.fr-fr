---
title: Message WM_DDE_ACK (DDE. h)
description: 'Le \_ \_ message d’accusé de réception DDE DDE avertit une application échange dynamique de données (DDE) de la réception et du traitement des messages suivants : WM \_ DDE \_ en attente, \_ exécution DDE WM \_ , \_ données DDE WM \_ , \_ notification DDE WM, notification DDE non- \_ \_ \_ notification, \_ lancement DDE WM \_ ou \_ requête DDE WM \_ (dans certains cas). Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.'
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032780"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="f14aa-105">Message d’accusé de réception DDE de WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="f14aa-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="f14aa-106">Le message d’accusé de réception **\_ DDE \_ DDE** notifie une application échange dynamique de données (DDE) de la réception et du traitement des messages suivants : [**WM \_ DDE \_**](wm-dde-poke.md)en attente, WM [**\_ DDE \_ Execute**](wm-dde-execute.md), WM DDE [**\_ \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ readvit**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiate**](wm-dde-initiate.md)ou [**WM \_ DDE \_ Request**](wm-dde-request.md) (dans certains cas).</span><span class="sxs-lookup"><span data-stu-id="f14aa-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="f14aa-107">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="f14aa-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="f14aa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f14aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f14aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f14aa-110">Lors de la réponse à l' [**\_ \_ initialisation**](wm-dde-initiate.md)de l’échange de messages WM, ce paramètre est un handle de la fenêtre de serveur qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="f14aa-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="f14aa-111">Lors de la réponse à l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), ce paramètre est un handle de la fenêtre de serveur qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="f14aa-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="f14aa-112">Lorsque vous répondez à tous les autres messages, ce paramètre est un handle vers la fenêtre du client ou du serveur qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="f14aa-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="f14aa-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f14aa-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f14aa-114">Lors de la réponse au lancement de l' [**\_ échange de liaison \_ WM**](wm-dde-initiate.md), le mot de poids faible contient un atome qui identifie l’application de réponse.</span><span class="sxs-lookup"><span data-stu-id="f14aa-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="f14aa-115">Le mot de poids fort contient un atome qui identifie la rubrique pour laquelle une conversation est établie.</span><span class="sxs-lookup"><span data-stu-id="f14aa-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="f14aa-116">Lors de la réponse à l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), le mot de poids faible spécifie une structure [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenant une série d’indicateurs qui indiquent l’état de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f14aa-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="f14aa-117">Le mot de poids fort est un handle vers un objet de mémoire globale qui contient la chaîne de commande qui a été reçue dans le message d' **\_ \_ exécution DDE de WM** .</span><span class="sxs-lookup"><span data-stu-id="f14aa-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="f14aa-118">Lors de la réponse à tous les autres messages, le mot de poids faible spécifie une structure [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenant une série d’indicateurs qui indiquent l’état de la réponse.</span><span class="sxs-lookup"><span data-stu-id="f14aa-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="f14aa-119">Le mot de poids fort contient un atome global qui identifie le nom de l’élément de données pour lequel la réponse est envoyée.</span><span class="sxs-lookup"><span data-stu-id="f14aa-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f14aa-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f14aa-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="f14aa-121">Publication</span><span class="sxs-lookup"><span data-stu-id="f14aa-121">Posting</span></span>

<span data-ttu-id="f14aa-122">À l’exception de la réponse au message de [**\_ \_ lancement DDE de WM**](wm-dde-initiate.md) , l’application publie le message d' **\_ \_ accusé** de réception DDE en appelant la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , et non en appelant la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="f14aa-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="f14aa-123">Lors de la réponse à l' **\_ \_ initialisation** de l’échange de messages WM, l’application envoie le message d’accusé de réception **\_ \_ DDE** en appelant **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="f14aa-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="f14aa-124">Dans ce cas, ni l’atome de nom d’application, ni l’atome de nom de rubrique ne doivent avoir la **valeur null** (même si le message « **WM \_ DDE \_ initiate** » spécifie des atomes **null** ).</span><span class="sxs-lookup"><span data-stu-id="f14aa-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="f14aa-125">Lors de la réception d’un message avec un Atom associé, la publication d’applications **WM \_ DDE \_ ACK** peut réutiliser l’atome qui accompagnait le message d’origine, ou il peut le supprimer et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="f14aa-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="f14aa-126">Lors de la reconnaissance de l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), l’application qui publie l' **\_ \_ accusé** de réception de l’échange de messages WM doit réutiliser l’objet mémoire globale identifié dans le message d’origine **WM \_ DDE \_ Execute** .</span><span class="sxs-lookup"><span data-stu-id="f14aa-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="f14aa-127">Tous les messages d’accusé de réception **\_ DDE \_ DDE** publiés doivent créer ou réutiliser le paramètre *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f14aa-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="f14aa-128">Si une application a initié l’arrêt d’une conversation en publiant le protocole [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) et est en attente de confirmation, l’application en attente ne doit pas accuser réception (positif ou négatif) des messages suivants envoyés par l’autre application.</span><span class="sxs-lookup"><span data-stu-id="f14aa-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="f14aa-129">L’application en attente doit supprimer tous les atomes ou objets de mémoire partagée reçus dans ces messages intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="f14aa-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="f14aa-130">Les objets de mémoire ne doivent pas être libérés si l’indicateur **fRelease** est défini sur **false** dans les messages de [**\_ \_ données**](wm-dde-data.md) d’interfonctionnement [**DDE de WM \_ \_**](wm-dde-poke.md) et de WM.</span><span class="sxs-lookup"><span data-stu-id="f14aa-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="f14aa-131">Réception</span><span class="sxs-lookup"><span data-stu-id="f14aa-131">Receiving</span></span>

<span data-ttu-id="f14aa-132">L’application qui reçoit un message « **WM \_ DDE \_ ACK** » doit supprimer tous les atomes accompagnant le message.</span><span class="sxs-lookup"><span data-stu-id="f14aa-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="f14aa-133">Si l’application reçoit un **\_ \_ accusé** de réception DDE de WM en réponse à un message avec un objet de mémoire globale associé, et que l’objet a été envoyé avec les indicateurs **fRelease** définis sur **false**, l’application est responsable de la suppression de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f14aa-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="f14aa-134">Si l’application reçoit un message **d' \_ \_ accusé** de réception DDE de WM négatif publié en réponse à un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages de ce fichier, l’application doit supprimer l’objet mémoire globale qui a été publié avec le message d' **\_ \_ avis DDE DDE** d’origine.</span><span class="sxs-lookup"><span data-stu-id="f14aa-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="f14aa-135">Si l’application reçoit un message **d' \_ \_ accusé** de réception DDE de WM négatif publié en réponse à une demande de données de l' [**échange de \_ \_ données (DDE**](wm-dde-data.md)) WM, à un message d’exécution DDE ou à un message d' [**\_ \_ exécution DDE**](wm-dde-execute.md) de WM, l’application doit supprimer l’objet mémoire globale qui est publié avec le message d’origine **WM \_ DDE \_ Data**, **WM \_ DDE \_** en attente ou **WM \_ DDE \_ Execute** . [**\_ \_**](wm-dde-poke.md)</span><span class="sxs-lookup"><span data-stu-id="f14aa-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="f14aa-136">L’application qui reçoit un message **d' \_ \_ accusé** de réception DDE de WM publié doit libérer le paramètre *lParam* à l’aide de la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f14aa-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f14aa-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f14aa-137">Requirements</span></span>



| <span data-ttu-id="f14aa-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f14aa-138">Requirement</span></span> | <span data-ttu-id="f14aa-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14aa-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f14aa-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14aa-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f14aa-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f14aa-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f14aa-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14aa-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f14aa-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f14aa-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f14aa-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="f14aa-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f14aa-145"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f14aa-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14aa-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14aa-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="f14aa-147">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f14aa-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f14aa-148">**DDEACK**</span><span class="sxs-lookup"><span data-stu-id="f14aa-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="f14aa-149">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f14aa-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="f14aa-150">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f14aa-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="f14aa-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f14aa-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f14aa-152">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f14aa-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="f14aa-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f14aa-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f14aa-154">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f14aa-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="f14aa-155">**\_avis DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f14aa-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="f14aa-156">**\_données DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f14aa-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="f14aa-157">**\_exécution DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f14aa-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="f14aa-158">**\_lancement de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f14aa-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="f14aa-159">**en-dessous du protocole WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="f14aa-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="f14aa-160">**\_requête DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f14aa-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="f14aa-161">**arrêt de l’échange de thread WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f14aa-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="f14aa-162">**informer de l' \_ échange de \_ notification**</span><span class="sxs-lookup"><span data-stu-id="f14aa-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="f14aa-163">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f14aa-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f14aa-164">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="f14aa-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

