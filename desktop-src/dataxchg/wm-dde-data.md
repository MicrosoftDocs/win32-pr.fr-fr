---
title: Message WM_DDE_DATA (DDE. h)
description: Une application serveur de échange dynamique de données (DDE) publie un \_ \_ message de données WM dans une application cliente DDE pour transmettre un élément de données au client ou pour informer le client de la disponibilité d’un élément de données.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513597"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="0aa78-104">\_Message de \_ données DDE WM</span><span class="sxs-lookup"><span data-stu-id="0aa78-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="0aa78-105">Une application serveur de échange dynamique de données (DDE) publie un message de **\_ \_ données WM** dans une application cliente DDE pour transmettre un élément de données au client ou pour informer le client de la disponibilité d’un élément de données.</span><span class="sxs-lookup"><span data-stu-id="0aa78-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="0aa78-106">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="0aa78-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="0aa78-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aa78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa78-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aa78-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa78-109">Handle de la fenêtre de serveur qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="0aa78-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="0aa78-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aa78-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa78-111">Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) avec les données et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0aa78-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="0aa78-112">Le descripteur doit être défini sur la valeur **null** si le serveur notifie au client que la valeur de l’élément de données a changé pendant une liaison de données à chaud.</span><span class="sxs-lookup"><span data-stu-id="0aa78-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="0aa78-113">Un lien à chaud est établi par le client qui envoie un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages (DDE) WM avec le bit **fDeferUpd** défini.</span><span class="sxs-lookup"><span data-stu-id="0aa78-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="0aa78-114">Le mot de poids fort contient un atome qui identifie l’élément de données pour lequel les données ou la notification sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="0aa78-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0aa78-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0aa78-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="0aa78-116">Publication</span><span class="sxs-lookup"><span data-stu-id="0aa78-116">Posting</span></span>

<span data-ttu-id="0aa78-117">L’application serveur alloue l’objet mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="0aa78-118">Elle alloue Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="0aa78-119">Le serveur doit créer ou réutiliser le paramètre de *lParam* de données de l' [](/windows/desktop/api/Dde/nf-dde-packddelparam) échange de **données ( \_ DDE \_ ) WM** en appelant la fonction PackDDElParam ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="0aa78-120">Si l’application réceptrice (cliente) répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif, l’application de publication (serveur) doit supprimer l’objet mémoire globale ; dans le cas contraire, le client doit supprimer l’objet après avoir extrait son contenu en appelant la fonction [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="0aa78-121">Si l’application serveur définit le membre **fRelease** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) sur **false**, le serveur est responsable de la suppression de l’objet lors de la réception d’un accusé de réception positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="0aa78-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="0aa78-122">L’application serveur ne doit pas définir à la fois les membres **fAckReq** et **fRelease** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) sur **false**.</span><span class="sxs-lookup"><span data-stu-id="0aa78-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="0aa78-123">Si les deux membres ont la valeur **false**, il est impossible pour le serveur de déterminer quand supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="0aa78-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="0aa78-124">Réception</span><span class="sxs-lookup"><span data-stu-id="0aa78-124">Receiving</span></span>

<span data-ttu-id="0aa78-125">Si **fAckReq** a la **valeur true**, l’application cliente doit envoyer le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour répondre positivement ou négativement.</span><span class="sxs-lookup"><span data-stu-id="0aa78-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="0aa78-126">Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le client peut réutiliser l’Atom ou le supprimer et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="0aa78-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="0aa78-127">Le client doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="0aa78-128">Si **fAckReq** a la **valeur false**, l’application cliente doit supprimer l’atome.</span><span class="sxs-lookup"><span data-stu-id="0aa78-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="0aa78-129">Si l’application de publication a spécifié l’objet de mémoire globale comme **null**, l’application réceptrice peut demander au serveur d’envoyer les données en publiant un message de [**\_ \_ demande de DDE WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa78-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="0aa78-130">Après le traitement d’un message de **\_ \_ données. WM DDE** dans lequel l’objet mémoire globale n’a pas la **valeur null**, le client doit libérer l’objet, sauf si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="0aa78-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="0aa78-131">Le membre **fRelease** a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="0aa78-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="0aa78-132">Le membre **fRelease** a la **valeur true**, mais l’application cliente répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="0aa78-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa78-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aa78-133">Requirements</span></span>



| <span data-ttu-id="0aa78-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aa78-134">Requirement</span></span> | <span data-ttu-id="0aa78-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aa78-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa78-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa78-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa78-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa78-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0aa78-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa78-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa78-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa78-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0aa78-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="0aa78-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa78-141"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa78-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa78-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa78-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aa78-143">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0aa78-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0aa78-144">**DDEDATA**</span><span class="sxs-lookup"><span data-stu-id="0aa78-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="0aa78-145">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="0aa78-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="0aa78-146">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="0aa78-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="0aa78-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="0aa78-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="0aa78-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="0aa78-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="0aa78-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="0aa78-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="0aa78-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="0aa78-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="0aa78-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="0aa78-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="0aa78-152">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="0aa78-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="0aa78-153">**\_avis DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="0aa78-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="0aa78-154">**en-dessous du protocole WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="0aa78-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="0aa78-155">**\_requête DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="0aa78-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="0aa78-156">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0aa78-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0aa78-157">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="0aa78-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

