---
title: Message WM_DDE_INITIATE (DDE. h)
description: Une application cliente échange dynamique de données (DDE) envoie un \_ message de lancement de l’échange de messages (DDE) WM \_ pour initier une conversation avec une application serveur qui répond aux noms d’application et de rubrique spécifiés.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384519"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="5daa0-104">\_Message de lancement DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="5daa0-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="5daa0-105">Une application cliente échange dynamique de données (DDE) envoie un message de **\_ \_ lancement** de l’échange de messages (DDE) WM pour initier une conversation avec une application serveur qui répond aux noms d’application et de rubrique spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5daa0-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="5daa0-106">Lors de la réception de ce message, toutes les applications serveur avec des noms qui correspondent à l’application spécifiée et qui prennent en charge la rubrique spécifiée sont censées la reconnaître.</span><span class="sxs-lookup"><span data-stu-id="5daa0-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="5daa0-107">(Pour plus d’informations, consultez le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM.)</span><span class="sxs-lookup"><span data-stu-id="5daa0-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="5daa0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5daa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5daa0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5daa0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5daa0-110">Handle de la fenêtre cliente qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="5daa0-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="5daa0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5daa0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5daa0-112">Le mot de poids faible contient un atome qui identifie l’application avec laquelle une conversation est demandée.</span><span class="sxs-lookup"><span data-stu-id="5daa0-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="5daa0-113">Le nom de l’application ne peut pas contenir de barres obliques (/) ou de barres obliques inverses ( \) .</span><span class="sxs-lookup"><span data-stu-id="5daa0-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="5daa0-114">Ces caractères sont réservés aux implémentations réseau.</span><span class="sxs-lookup"><span data-stu-id="5daa0-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="5daa0-115">Si ce paramètre a la **valeur null**, une conversation avec toutes les applications est demandée.</span><span class="sxs-lookup"><span data-stu-id="5daa0-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="5daa0-116">Le mot de poids fort contient un atome qui identifie la rubrique pour laquelle une conversation est demandée.</span><span class="sxs-lookup"><span data-stu-id="5daa0-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="5daa0-117">Si la rubrique est **null**, les conversations pour toutes les rubriques disponibles sont demandées.</span><span class="sxs-lookup"><span data-stu-id="5daa0-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5daa0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5daa0-118">Remarks</span></span>

<span data-ttu-id="5daa0-119">Si le mot de poids faible de *lParam* est **null**, toute application serveur peut répondre.</span><span class="sxs-lookup"><span data-stu-id="5daa0-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="5daa0-120">Si le mot de poids fort de *lParam* est **null**, toute rubrique est valide.</span><span class="sxs-lookup"><span data-stu-id="5daa0-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="5daa0-121">Lors de la réception d’une requête de **\_ \_ lancement DDE WM** avec le mot de poids fort du paramètre *lParam* défini sur **null**, un serveur doit envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour chacune des rubriques qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5daa0-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="5daa0-122">Envoi</span><span class="sxs-lookup"><span data-stu-id="5daa0-122">Sending</span></span>

<span data-ttu-id="5daa0-123">Le client diffuse le message à toutes les fenêtres de niveau supérieur en définissant le premier paramètre de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) sur la **\_ diffusion HWND**.</span><span class="sxs-lookup"><span data-stu-id="5daa0-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="5daa0-124">Si l’application cliente a déjà obtenu le descripteur de fenêtre du serveur souhaité, elle peut envoyer un lancement de l' **\_ échange de \_ liaison** de script WM directement à la fenêtre du serveur en passant le handle de fenêtre du serveur comme premier paramètre de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="5daa0-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="5daa0-125">L’application cliente alloue des atomes en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="5daa0-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="5daa0-126">Lorsque [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourne, l’application cliente doit supprimer les atomes.</span><span class="sxs-lookup"><span data-stu-id="5daa0-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="5daa0-127">Réception</span><span class="sxs-lookup"><span data-stu-id="5daa0-127">Receiving</span></span>

<span data-ttu-id="5daa0-128">Pour terminer l’initiation d’une conversation, l’application serveur doit répondre avec un ou plusieurs messages de l' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM, où chaque message est destiné à une rubrique distincte.</span><span class="sxs-lookup"><span data-stu-id="5daa0-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="5daa0-129">Lors de l’envoi d’un message d' **\_ \_ accusé** de réception DDE, le serveur doit créer des atomes ; il ne doit pas réutiliser les atomes envoyés avec l' **\_ \_ initialisation DDE WM**.</span><span class="sxs-lookup"><span data-stu-id="5daa0-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5daa0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5daa0-130">Requirements</span></span>



| <span data-ttu-id="5daa0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5daa0-131">Requirement</span></span> | <span data-ttu-id="5daa0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5daa0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5daa0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5daa0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5daa0-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5daa0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5daa0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5daa0-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5daa0-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5daa0-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="5daa0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5daa0-138"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5daa0-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5daa0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5daa0-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="5daa0-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5daa0-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5daa0-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="5daa0-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="5daa0-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="5daa0-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="5daa0-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5daa0-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="5daa0-144">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="5daa0-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="5daa0-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5daa0-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5daa0-146">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="5daa0-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

