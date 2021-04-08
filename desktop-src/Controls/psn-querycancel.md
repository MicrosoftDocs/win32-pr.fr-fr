---
title: PSN_QUERYCANCEL le code de notification (Prsht. h)
description: Indique que l’utilisateur a annulé la feuille de propriétés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- Contrôles Windows de code de notification PSN_QUERYCANCEL
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942019"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="9fac2-105">\_Code de notification PSN QUERYCANCEL</span><span class="sxs-lookup"><span data-stu-id="9fac2-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="9fac2-106">Indique que l’utilisateur a annulé la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9fac2-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="9fac2-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9fac2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="9fac2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fac2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fac2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fac2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fac2-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="9fac2-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="9fac2-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9fac2-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="9fac2-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="9fac2-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fac2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fac2-113">Return value</span></span>

<span data-ttu-id="9fac2-114">Retourne la **valeur true** pour empêcher l’opération d’annulation, ou **false** pour l’autoriser.</span><span class="sxs-lookup"><span data-stu-id="9fac2-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fac2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9fac2-115">Remarks</span></span>

<span data-ttu-id="9fac2-116">Ce code de notification est généralement envoyé lorsqu’un utilisateur clique sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="9fac2-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="9fac2-117">Elle est également envoyée lorsqu’un utilisateur clique sur le bouton **X** dans l’angle supérieur droit de la feuille de propriétés ou appuie sur la touche ÉCHAP.</span><span class="sxs-lookup"><span data-stu-id="9fac2-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="9fac2-118">Une page de feuille de propriétés peut gérer ce code de notification pour demander à l’utilisateur de vérifier l’opération d’annulation.</span><span class="sxs-lookup"><span data-stu-id="9fac2-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="9fac2-119">Pour définir une valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur de retour de la fonction \_ MSGRESULT.</span><span class="sxs-lookup"><span data-stu-id="9fac2-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="9fac2-120">La procédure de la boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="9fac2-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fac2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fac2-121">Requirements</span></span>



| <span data-ttu-id="9fac2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fac2-122">Requirement</span></span> | <span data-ttu-id="9fac2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fac2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fac2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fac2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9fac2-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fac2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fac2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fac2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9fac2-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fac2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fac2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fac2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fac2-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fac2-129"><dt>Prsht.h</dt></span></span> </dl> |



 

