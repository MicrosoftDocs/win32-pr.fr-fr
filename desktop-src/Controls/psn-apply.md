---
title: PSN_APPLY le code de notification (Prsht. h)
description: Envoyé à chaque page de la feuille de propriétés pour indiquer que l’utilisateur a cliqué sur le bouton OK, fermer ou appliquer et souhaite que toutes les modifications soient prises en compte. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- Contrôles Windows de code de notification PSN_APPLY
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465862"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="6589b-105">PSN \_ appliquer le code de notification</span><span class="sxs-lookup"><span data-stu-id="6589b-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="6589b-106">Envoyé à chaque page de la feuille de propriétés pour indiquer que l’utilisateur a cliqué sur le bouton OK, fermer ou appliquer et souhaite que toutes les modifications soient prises en compte.</span><span class="sxs-lookup"><span data-stu-id="6589b-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="6589b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6589b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6589b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6589b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6589b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6589b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6589b-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification, y compris l’ID de la page.</span><span class="sxs-lookup"><span data-stu-id="6589b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6589b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6589b-111">Return value</span></span>

<span data-ttu-id="6589b-112">Définissez PSNRET \_ NOERROR pour indiquer que les modifications apportées à cette page sont valides et ont été appliquées.</span><span class="sxs-lookup"><span data-stu-id="6589b-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="6589b-113">Si toutes les pages définissent PSNRET \_ NOERROR, la feuille de propriétés peut être détruite.</span><span class="sxs-lookup"><span data-stu-id="6589b-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="6589b-114">Pour indiquer que les modifications apportées à cette page ne sont pas valides et que la feuille de propriétés n’est pas détruite, définissez l’une des valeurs de retour suivantes :</span><span class="sxs-lookup"><span data-stu-id="6589b-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="6589b-115">PSNRET \_ non valide.</span><span class="sxs-lookup"><span data-stu-id="6589b-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="6589b-116">La feuille de propriétés ne sera pas détruite et le focus sera renvoyé à cette page.</span><span class="sxs-lookup"><span data-stu-id="6589b-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="6589b-117">PSNRET \_ non valide \_ NOCHANGEPAGE.</span><span class="sxs-lookup"><span data-stu-id="6589b-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="6589b-118">La feuille de propriétés ne sera pas détruite et le focus sera retourné à la page qui avait le focus lorsque le bouton était enfoncé.</span><span class="sxs-lookup"><span data-stu-id="6589b-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="6589b-119">Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la \_ valeur de MSGRESULT DWL, et la procédure de boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="6589b-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6589b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6589b-120">Remarks</span></span>

<span data-ttu-id="6589b-121">Quand l’utilisateur clique sur le bouton OK, appliquer ou fermer, la feuille de propriétés envoie une notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page active, ce qui lui donne la possibilité de valider les modifications de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6589b-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="6589b-122">Si les modifications sont valides, la feuille de propriétés envoie un \_ Code de notification d’application PSN à chaque page, en la dirigeant pour appliquer les nouvelles propriétés à l’élément correspondant.</span><span class="sxs-lookup"><span data-stu-id="6589b-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="6589b-123">La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification d’application PSN est envoyé.</span><span class="sxs-lookup"><span data-stu-id="6589b-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="6589b-124">N’essayez pas d’ajouter, de supprimer ou d’insérer des pages pendant la gestion de cette notification.</span><span class="sxs-lookup"><span data-stu-id="6589b-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="6589b-125">Vous obtiendrez des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="6589b-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="6589b-126">Le membre **lParam** de la structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) vers laquelle pointe *lParam* prend la valeur **true** si l’utilisateur clique sur le bouton OK.</span><span class="sxs-lookup"><span data-stu-id="6589b-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="6589b-127">Elle est également définie sur **true** si le message [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) a été envoyé et que l’utilisateur clique sur le bouton Fermer.</span><span class="sxs-lookup"><span data-stu-id="6589b-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="6589b-128">Elle a la valeur **false** si l’utilisateur clique sur le bouton appliquer.</span><span class="sxs-lookup"><span data-stu-id="6589b-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="6589b-129">La structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6589b-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="6589b-130">N’appelez pas la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) lors du traitement de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="6589b-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="6589b-131">Une feuille de propriétés modale est détruite si l’utilisateur clique sur le bouton OK et que chaque page retourne la \_ valeur d’erreur noPSNRET en réponse à **PSN \_ apply**.</span><span class="sxs-lookup"><span data-stu-id="6589b-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="6589b-132">Si une page retourne un \_ NOCHANGEPAGE non valide PSNRET ou PSNRET \_ non valide \_ , le processus d’application est immédiatement annulé.</span><span class="sxs-lookup"><span data-stu-id="6589b-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="6589b-133">Les pages après la page d’annulation ne recevront pas de \_ Code de notification d’application PSN.</span><span class="sxs-lookup"><span data-stu-id="6589b-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="6589b-134">Pour recevoir ce code de notification, une page doit définir la \_ valeur DWL MSGRESULT sur **false** en réponse au code de notification [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="6589b-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="6589b-135">Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="6589b-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6589b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6589b-136">Requirements</span></span>



| <span data-ttu-id="6589b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6589b-137">Requirement</span></span> | <span data-ttu-id="6589b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="6589b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6589b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6589b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6589b-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6589b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6589b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6589b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6589b-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6589b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6589b-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="6589b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6589b-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6589b-144"><dt>Prsht.h</dt></span></span> </dl> |



 

