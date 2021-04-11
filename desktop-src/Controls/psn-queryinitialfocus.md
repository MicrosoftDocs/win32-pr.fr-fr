---
title: PSN_QUERYINITIALFOCUS le code de notification (Prsht. h)
description: Envoyé par une feuille de propriétés pour permettre à une page de feuille de propriétés de spécifier quel contrôle de boîte de dialogue doit recevoir le focus initial. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Contrôles Windows de code de notification PSN_QUERYINITIALFOCUS
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102973"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="0b8a2-105">\_Code de notification PSN QUERYINITIALFOCUS</span><span class="sxs-lookup"><span data-stu-id="0b8a2-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="0b8a2-106">Envoyé par une feuille de propriétés pour permettre à une page de feuille de propriétés de spécifier quel contrôle de boîte de dialogue doit recevoir le focus initial.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="0b8a2-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0b8a2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0b8a2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b8a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b8a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b8a2-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) .</span><span class="sxs-lookup"><span data-stu-id="0b8a2-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="0b8a2-111">Effectuez un cast du membre **lParam** de cette structure en un type **HWND** , pour récupérer le handle du contrôle qui reçoit le focus par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="0b8a2-112">La structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b8a2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b8a2-113">Return value</span></span>

<span data-ttu-id="0b8a2-114">Pour spécifier le contrôle qui doit recevoir le focus, retournez le handle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="0b8a2-115">Sinon, retournez zéro et le focus sera placé dans le contrôle par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="0b8a2-116">Pour définir la valeur de retour, la procédure de la boîte de dialogue doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec une valeur **\_ MSGRESULT DWL** et retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8a2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0b8a2-117">Remarks</span></span>

<span data-ttu-id="0b8a2-118">Une application ne doit pas appeler la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) lors de la gestion de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="0b8a2-119">Retourne le handle du contrôle qui doit recevoir le focus, et le gestionnaire de feuille de propriétés gère la modification du focus.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="0b8a2-120">Le \_ Code de notification PSN QUERYINITIALFOCUS n’est pas envoyé si le gestionnaire de feuille de propriétés détermine qu’aucun contrôle de la page ne doit recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="0b8a2-121">Ce fragment de code implémente un gestionnaire simple pour PSN \_ QUERYINITIALFOCUS.</span><span class="sxs-lookup"><span data-stu-id="0b8a2-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="0b8a2-122">Elle demande que le focus initial soit donné au contrôle d’emplacement **( \_ emplacement IDC**).</span><span class="sxs-lookup"><span data-stu-id="0b8a2-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="0b8a2-123">Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="0b8a2-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b8a2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b8a2-124">Requirements</span></span>



| <span data-ttu-id="0b8a2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b8a2-125">Requirement</span></span> | <span data-ttu-id="0b8a2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b8a2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8a2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b8a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b8a2-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b8a2-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b8a2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b8a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b8a2-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b8a2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0b8a2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b8a2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b8a2-132"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b8a2-132"><dt>Prsht.h</dt></span></span> </dl> |



 

