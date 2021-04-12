---
title: Message WM_DDE_ADVISE (DDE. h)
description: Une application cliente échange dynamique de données (DDE) publie le message de notification de l’échange de données (DDE) WM \_ \_ dans une application de serveur DDE pour demander au serveur de fournir une mise à jour pour un élément de données à chaque modification de l’élément.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103517"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="f9a5f-104">\_Message de \_ notification DDE WM</span><span class="sxs-lookup"><span data-stu-id="f9a5f-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="f9a5f-105">Une application cliente échange dynamique de données (DDE) publie le message de **\_ \_ notification** de l’échange de données (DDE) WM dans une application de serveur DDE pour demander au serveur de fournir une mise à jour pour un élément de données à chaque modification de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="f9a5f-106">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="f9a5f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9a5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a5f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9a5f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a5f-109">Handle de la fenêtre client qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="f9a5f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9a5f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a5f-111">Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) qui spécifie la façon dont les données doivent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="f9a5f-112">Le mot de poids fort contient un atome qui identifie l’élément de données demandé.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9a5f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f9a5f-113">Remarks</span></span>

<span data-ttu-id="f9a5f-114">Si une application cliente prend en charge plusieurs formats de presse-papiers pour une seule rubrique et un seul élément, elle peut envoyer plusieurs messages de **\_ \_ notification** de l’échange de message pour la rubrique et l’élément, en spécifiant un format de presse-papiers différent pour chaque message.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="f9a5f-115">Notez qu’un serveur peut prendre en charge plusieurs formats uniquement pour les liaisons de données à chaud, et non pour les liaisons de données à chaud.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="f9a5f-116">Publication</span><span class="sxs-lookup"><span data-stu-id="f9a5f-116">Posting</span></span>

<span data-ttu-id="f9a5f-117">L’application cliente publie le message de **\_ \_ notification** de l’échange de messages avec le protocole WM en appelant la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , et non la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="f9a5f-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="f9a5f-118">L’application cliente alloue l’objet mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="f9a5f-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="f9a5f-119">Elle alloue Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="f9a5f-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="f9a5f-120">L’application cliente doit créer ou réutiliser le paramètre **WM \_ DDE \_ Advise** *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f9a5f-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="f9a5f-121">Si l’application réceptrice (serveur) répond avec un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif, l’application de publication doit supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="f9a5f-122">L’indicateur **fRelease** n’est pas utilisé dans les messages de **\_ \_ notification DDE de WM** , mais leur comportement de libération de données est similaire à celui des données de l’échange de [**\_ \_ données (DDE) WM**](wm-dde-data.md) et des messages d’entourage de données par le biais de la **propriété** **fRelease** . [**\_ \_**](wm-dde-poke.md)</span><span class="sxs-lookup"><span data-stu-id="f9a5f-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="f9a5f-123">Réception</span><span class="sxs-lookup"><span data-stu-id="f9a5f-123">Receiving</span></span>

<span data-ttu-id="f9a5f-124">L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="f9a5f-125">Lors de la publication de l' **\_ \_ accusé** de réception DDE de WM, l’application peut réutiliser l’Atom ou le supprimer et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="f9a5f-126">Si le message d’accusé de réception **\_ DDE DDE \_** est positif, l’application doit supprimer l’objet mémoire globale ; dans le cas contraire, l’application ne doit pas supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="f9a5f-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="f9a5f-127">Le serveur doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f9a5f-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a5f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9a5f-128">Requirements</span></span>



| <span data-ttu-id="f9a5f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9a5f-129">Requirement</span></span> | <span data-ttu-id="f9a5f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a5f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a5f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9a5f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a5f-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9a5f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9a5f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9a5f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a5f-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9a5f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9a5f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9a5f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9a5f-136"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5f-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a5f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9a5f-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9a5f-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9a5f-139">**DDEADVISE**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="f9a5f-140">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="f9a5f-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="f9a5f-142">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="f9a5f-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f9a5f-144">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="f9a5f-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f9a5f-146">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="f9a5f-147">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="f9a5f-148">**\_données DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="f9a5f-149">**en-dessous du protocole WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="f9a5f-150">**\_requête DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="f9a5f-151">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f9a5f-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f9a5f-152">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="f9a5f-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

