---
title: PSN_TRANSLATEACCELERATOR le code de notification (Prsht. h)
description: Avertit une feuille de propriétés qu’un message de clavier a été reçu. Elle offre la possibilité d’effectuer une traduction d’accélérateur de clavier privée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Contrôles Windows de code de notification PSN_TRANSLATEACCELERATOR
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510934"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="549ba-106">\_Code de notification PSN TRANSLATEACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="549ba-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="549ba-107">Avertit une feuille de propriétés qu’un message de clavier a été reçu.</span><span class="sxs-lookup"><span data-stu-id="549ba-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="549ba-108">Elle offre la possibilité d’effectuer une traduction d’accélérateur de clavier privée.</span><span class="sxs-lookup"><span data-stu-id="549ba-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="549ba-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="549ba-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="549ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="549ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="549ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="549ba-112">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="549ba-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="549ba-113">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de la structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="549ba-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="549ba-114">Le membre **lParam** de la structure **PSHNOTIFY** est un pointeur vers le [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)du message.</span><span class="sxs-lookup"><span data-stu-id="549ba-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="549ba-115">Elle peut être convertie en type **LPMSG** , pour accéder aux paramètres du message à traduire.</span><span class="sxs-lookup"><span data-stu-id="549ba-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549ba-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="549ba-116">Return value</span></span>

<span data-ttu-id="549ba-117">Retourne PSNRET \_ MESSAGEHANDLED pour indiquer qu’aucun traitement supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="549ba-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="549ba-118">Retourne une \_ erreur PSNRET pour demander un traitement normal.</span><span class="sxs-lookup"><span data-stu-id="549ba-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="549ba-119">Notes</span><span class="sxs-lookup"><span data-stu-id="549ba-119">Remarks</span></span>

<span data-ttu-id="549ba-120">Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de l’DWL \_ .</span><span class="sxs-lookup"><span data-stu-id="549ba-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="549ba-121">La procédure de la boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="549ba-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="549ba-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="549ba-122">Requirements</span></span>



| <span data-ttu-id="549ba-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="549ba-123">Requirement</span></span> | <span data-ttu-id="549ba-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="549ba-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="549ba-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="549ba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="549ba-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="549ba-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="549ba-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="549ba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="549ba-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="549ba-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="549ba-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="549ba-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="549ba-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="549ba-130"><dt>Prsht.h</dt></span></span> </dl> |



 

