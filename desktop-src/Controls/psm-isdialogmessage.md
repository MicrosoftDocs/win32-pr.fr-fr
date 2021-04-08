---
title: Message PSM_ISDIALOGMESSAGE (Prsht. h)
description: Transmet un message à une boîte de dialogue de feuille de propriétés et indique si la boîte de dialogue a traité le message. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843661"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="88b44-105">\_Message PSM ISDIALOGMESSAGE</span><span class="sxs-lookup"><span data-stu-id="88b44-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="88b44-106">Transmet un message à une boîte de dialogue de feuille de propriétés et indique si la boîte de dialogue a traité le message.</span><span class="sxs-lookup"><span data-stu-id="88b44-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="88b44-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .</span><span class="sxs-lookup"><span data-stu-id="88b44-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="88b44-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88b44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88b44-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88b44-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="88b44-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="88b44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88b44-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88b44-112">Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message à vérifier.</span><span class="sxs-lookup"><span data-stu-id="88b44-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b44-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88b44-113">Return value</span></span>

<span data-ttu-id="88b44-114">Retourne la **valeur true** si le message a été traité, ou **false** si le message n’a pas été traité.</span><span class="sxs-lookup"><span data-stu-id="88b44-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b44-115">Notes</span><span class="sxs-lookup"><span data-stu-id="88b44-115">Remarks</span></span>

<span data-ttu-id="88b44-116">Votre boucle de messages doit utiliser le message **\_ ISDIALOGMESSAGE PSM** avec les feuilles de propriétés non modales pour transmettre les messages à la boîte de dialogue de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88b44-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="88b44-117">Sur les systèmes qui prennent en charge Unicode, utilisez les versions Unicode des fonctions [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) et [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** et **PeekMessageW**) pour récupérer les messages.</span><span class="sxs-lookup"><span data-stu-id="88b44-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="88b44-118">Si la valeur de retour indique que le message a été traité, il ne doit pas être passé à la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="88b44-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="88b44-119">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="88b44-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88b44-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88b44-120">Requirements</span></span>



| <span data-ttu-id="88b44-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88b44-121">Requirement</span></span> | <span data-ttu-id="88b44-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="88b44-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88b44-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88b44-123">Minimum supported client</span></span><br/> | <span data-ttu-id="88b44-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88b44-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="88b44-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88b44-125">Minimum supported server</span></span><br/> | <span data-ttu-id="88b44-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88b44-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="88b44-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="88b44-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b44-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="88b44-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b44-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88b44-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b44-130">**Feuille**</span><span class="sxs-lookup"><span data-stu-id="88b44-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

