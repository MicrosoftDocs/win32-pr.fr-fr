---
title: PSN_KILLACTIVE le code de notification (Prsht. h)
description: Avertit une page qu’il va perdre l’activation soit parce qu’une autre page est activée, soit parce que l’utilisateur a cliqué sur le bouton OK. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Contrôles Windows de code de notification PSN_KILLACTIVE
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942021"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="ea94d-105">\_Code de notification PSN KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="ea94d-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="ea94d-106">Avertit une page qu’il va perdre l’activation soit parce qu’une autre page est activée, soit parce que l’utilisateur a cliqué sur le bouton OK.</span><span class="sxs-lookup"><span data-stu-id="ea94d-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="ea94d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ea94d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ea94d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea94d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea94d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea94d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea94d-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ea94d-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="ea94d-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ea94d-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="ea94d-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="ea94d-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea94d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea94d-113">Return value</span></span>

<span data-ttu-id="ea94d-114">Retourne la **valeur true** pour empêcher la page de perdre l’activation, ou **false** pour l’autoriser.</span><span class="sxs-lookup"><span data-stu-id="ea94d-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea94d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ea94d-115">Remarks</span></span>

<span data-ttu-id="ea94d-116">Une application gère ce code de notification pour valider les informations entrées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea94d-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="ea94d-117">La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification PSN KILLACTIVE est envoyé.</span><span class="sxs-lookup"><span data-stu-id="ea94d-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="ea94d-118">N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="ea94d-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="ea94d-119">Vous obtiendrez des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="ea94d-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="ea94d-120">Pour définir une valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec une valeur MSGRESULT de l’DWL \_ définie sur la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ea94d-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="ea94d-121">La procédure de la boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="ea94d-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="ea94d-122">Si la procédure de la boîte de dialogue affecte la \_ **valeur true** à DWL MSGRESULT, une boîte de message doit s’afficher pour expliquer le problème à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea94d-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea94d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea94d-123">Requirements</span></span>



| <span data-ttu-id="ea94d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea94d-124">Requirement</span></span> | <span data-ttu-id="ea94d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea94d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea94d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea94d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea94d-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea94d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ea94d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea94d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea94d-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea94d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea94d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea94d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea94d-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea94d-131"><dt>Prsht.h</dt></span></span> </dl> |



 

