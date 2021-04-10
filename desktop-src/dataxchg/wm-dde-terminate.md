---
title: Message WM_DDE_TERMINATE (DDE. h)
description: Une application échange dynamique de données (DDE) (client ou serveur) publie un \_ message WM DDE \_ Terminate pour mettre fin à une conversation. Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103413"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="c3c5d-105">Message de fin du \_ DDE WM \_</span><span class="sxs-lookup"><span data-stu-id="c3c5d-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="c3c5d-106">Une application échange dynamique de données (DDE) (client ou serveur) publie un message **WM \_ DDE \_ Terminate** pour mettre fin à une conversation.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="c3c5d-107">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="c3c5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3c5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3c5d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3c5d-110">Handle de la fenêtre du client ou du serveur qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3c5d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3c5d-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3c5d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c3c5d-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="c3c5d-114">Publication</span><span class="sxs-lookup"><span data-stu-id="c3c5d-114">Posting</span></span>

<span data-ttu-id="c3c5d-115">Lors de l’attente de la confirmation de la résiliation, l’application de publication ne doit pas publier d’autres messages dans l’application réceptrice.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="c3c5d-116">Si l’application émettrice reçoit des messages (autres **que \_ WM DDE \_ Terminate**) à partir de l’application réceptrice, elle doit supprimer tous les atomes ou objets de mémoire partagée qui accompagnent les messages, à l’exception des objets de mémoire globale associés à des messages de données d’interception [**\_ DDE \_**](wm-dde-poke.md) ou de [**\_ \_ données DDE WM**](wm-dde-data.md) qui n’ont pas de membre **fRelease** défini.</span><span class="sxs-lookup"><span data-stu-id="c3c5d-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="c3c5d-117">Réception</span><span class="sxs-lookup"><span data-stu-id="c3c5d-117">Receiving</span></span>

<span data-ttu-id="c3c5d-118">L’application cliente ou serveur doit répondre en publiant un message **WM \_ DDE \_ Terminate** .</span><span class="sxs-lookup"><span data-stu-id="c3c5d-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c5d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3c5d-119">Requirements</span></span>



| <span data-ttu-id="c3c5d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3c5d-120">Requirement</span></span> | <span data-ttu-id="c3c5d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3c5d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c5d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c5d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c5d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3c5d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3c5d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c5d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c5d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3c5d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3c5d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3c5d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c5d-127"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3c5d-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c5d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3c5d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3c5d-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3c5d-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="c3c5d-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="c3c5d-132">**\_données DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="c3c5d-133">**en-dessous du protocole WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="c3c5d-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c3c5d-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c3c5d-135">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="c3c5d-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

