---
title: Message WM_DDE_POKE (DDE. h)
description: Une application cliente de échange dynamique de données (DDE) publie un message de l’application de \_ \_ serveur de publication DDE dans une application de serveur DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743693"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="53c42-104">Message d’échange de messages de l' \_ échange WM \_</span><span class="sxs-lookup"><span data-stu-id="53c42-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="53c42-105">Une application cliente de échange dynamique de données (DDE) publie un message de l’application de serveur de publication DDE dans une application de serveur DDE. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="53c42-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="53c42-106">Un client utilise ce message pour demander au serveur d’accepter un élément de données non sollicité.</span><span class="sxs-lookup"><span data-stu-id="53c42-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="53c42-107">Le serveur doit répondre avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE qui indique s’il a accepté l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="53c42-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="53c42-108">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="53c42-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="53c42-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53c42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c42-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53c42-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53c42-111">Handle de la fenêtre client qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="53c42-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="53c42-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53c42-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53c42-113">Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) avec les données et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="53c42-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="53c42-114">Le mot de poids fort contient un atome global qui identifie l’élément de données pour lequel les données ou la notification sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="53c42-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53c42-115">Notes</span><span class="sxs-lookup"><span data-stu-id="53c42-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="53c42-116">Publication</span><span class="sxs-lookup"><span data-stu-id="53c42-116">Posting</span></span>

<span data-ttu-id="53c42-117">L’application cliente doit allouer de la mémoire pour l’objet de mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="53c42-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="53c42-118">L’application cliente doit supprimer l’objet si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="53c42-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="53c42-119">L’application serveur répond avec un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="53c42-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="53c42-120">Le membre **fRelease** a la **valeur false**, mais l’application serveur répond avec un [**\_ \_ accusé**](wm-dde-ack.md)de réception DDE positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="53c42-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="53c42-121">L’application cliente doit créer Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="53c42-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="53c42-122">L’application cliente doit créer ou réutiliser le paramètre de la fonction *lParam* de l' **échange de liaison ( \_ DDE \_ ) WM** en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="53c42-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="53c42-123">Réception</span><span class="sxs-lookup"><span data-stu-id="53c42-123">Receiving</span></span>

<span data-ttu-id="53c42-124">L’application serveur doit envoyer le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour répondre positivement ou négativement.</span><span class="sxs-lookup"><span data-stu-id="53c42-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="53c42-125">Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le serveur peut réutiliser l’Atom ou le supprimer et en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="53c42-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="53c42-126">Le serveur doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="53c42-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="53c42-127">Pour libérer l’objet mémoire globale, le serveur doit appeler la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="53c42-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="53c42-128">En outre, si le format de données est [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) ou **CF \_ MetaFilePict**, le serveur doit également appeler [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) avec le descripteur de métafichier incorporé.</span><span class="sxs-lookup"><span data-stu-id="53c42-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="53c42-129">Ces deux formats ont un niveau supplémentaire d’indirection ; autrement dit, une application doit verrouiller l’objet pour obtenir un pointeur vers un handle, puis verrouiller ce handle pour obtenir un pointeur vers une structure [**MetaFilePict**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) et enfin appeler **DeleteMetaFile** avec le handle à partir du membre **hMF** de la structure **MetaFilePict** .</span><span class="sxs-lookup"><span data-stu-id="53c42-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="53c42-130">Pour libérer l’objet, le serveur doit appeler la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="53c42-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c42-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53c42-131">Requirements</span></span>



| <span data-ttu-id="53c42-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53c42-132">Requirement</span></span> | <span data-ttu-id="53c42-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c42-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c42-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c42-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53c42-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c42-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="53c42-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c42-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53c42-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c42-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53c42-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="53c42-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c42-139"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53c42-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c42-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c42-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="53c42-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="53c42-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53c42-142">**DDEPOKE**</span><span class="sxs-lookup"><span data-stu-id="53c42-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="53c42-143">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="53c42-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="53c42-144">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="53c42-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="53c42-145">**METAFILEPICT**</span><span class="sxs-lookup"><span data-stu-id="53c42-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="53c42-146">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="53c42-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="53c42-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="53c42-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="53c42-148">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="53c42-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="53c42-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="53c42-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="53c42-150">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="53c42-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="53c42-151">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="53c42-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="53c42-152">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="53c42-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53c42-153">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="53c42-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

