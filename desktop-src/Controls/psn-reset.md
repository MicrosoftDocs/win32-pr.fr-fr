---
title: PSN_RESET le code de notification (Prsht. h)
description: Avertit une page que la feuille de propriétés va être détruite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- Contrôles Windows de code de notification PSN_RESET
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512787"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="962ab-105">\_Code de notification de réinitialisation PSN</span><span class="sxs-lookup"><span data-stu-id="962ab-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="962ab-106">Avertit une page que la feuille de propriétés va être détruite.</span><span class="sxs-lookup"><span data-stu-id="962ab-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="962ab-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="962ab-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="962ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="962ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="962ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="962ab-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="962ab-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962ab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="962ab-111">Return value</span></span>

<span data-ttu-id="962ab-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="962ab-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="962ab-113">Notes</span><span class="sxs-lookup"><span data-stu-id="962ab-113">Remarks</span></span>

<span data-ttu-id="962ab-114">Toutes les modifications apportées depuis le dernier code de notification d' [ \_ application PSN](psn-apply.md) sont annulées, sauf dans le cas de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), qui ne prend pas en charge ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="962ab-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="962ab-115">Le membre **lParam** de la structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) vers laquelle pointe *lParam* prend la valeur **true** si l’utilisateur a cliqué sur le bouton **X** dans l’angle supérieur droit de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="962ab-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="962ab-116">La valeur est **false** si l’utilisateur a cliqué sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="962ab-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="962ab-117">La structure **PSHNOTIFY** contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="962ab-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="962ab-118">Une application peut utiliser ce code de notification comme opportunité d’effectuer des opérations de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="962ab-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="962ab-119">La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification de réinitialisation PSN est envoyé.</span><span class="sxs-lookup"><span data-stu-id="962ab-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="962ab-120">N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="962ab-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="962ab-121">Vous obtiendrez des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="962ab-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="962ab-122">N’appelez pas la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) lors du traitement de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="962ab-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="962ab-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="962ab-123">Requirements</span></span>



| <span data-ttu-id="962ab-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="962ab-124">Requirement</span></span> | <span data-ttu-id="962ab-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="962ab-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="962ab-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="962ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="962ab-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="962ab-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="962ab-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="962ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="962ab-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="962ab-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="962ab-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="962ab-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="962ab-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="962ab-131"><dt>Prsht.h</dt></span></span> </dl> |



 

