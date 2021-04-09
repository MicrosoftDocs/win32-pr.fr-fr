---
title: PSN_GETOBJECT le code de notification (Prsht. h)
description: Envoyé par une feuille de propriétés pour demander un objet cible de dépôt lorsque le curseur passe sur l’un des boutons du contrôle onglet. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- Contrôles Windows de code de notification PSN_GETOBJECT
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032564"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="70010-105">\_Code de notification PSN GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="70010-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="70010-106">Envoyé par une feuille de propriétés pour demander un objet cible de dépôt lorsque le curseur passe sur l’un des boutons du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="70010-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="70010-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="70010-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="70010-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70010-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70010-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70010-110">Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui, à l’entrée, contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="70010-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="70010-111">Si ce code de notification est traité, vous devez insérer les informations relatives à l’objet dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="70010-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70010-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70010-112">Return value</span></span>

<span data-ttu-id="70010-113">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="70010-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="70010-114">Notes</span><span class="sxs-lookup"><span data-stu-id="70010-114">Remarks</span></span>

<span data-ttu-id="70010-115">Pour fournir un objet, une application doit définir des valeurs dans certains membres de la structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) au niveau de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="70010-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="70010-116">Le membre **pObject** doit être défini sur un pointeur d’objet valide et le membre **HRESULT** doit être défini sur un indicateur de réussite.</span><span class="sxs-lookup"><span data-stu-id="70010-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="70010-117">Pour se conformer aux normes COM (Component Object Model), incrémentez toujours le nombre de références de l’objet lors de la fourniture d’un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="70010-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="70010-118">Si une application ne fournit pas d’objet, elle doit affecter la valeur **null** à **pObject** et **HRESULT** à un indicateur d’échec.</span><span class="sxs-lookup"><span data-stu-id="70010-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="70010-119">Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="70010-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70010-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70010-120">Requirements</span></span>



| <span data-ttu-id="70010-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70010-121">Requirement</span></span> | <span data-ttu-id="70010-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70010-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70010-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70010-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70010-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70010-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="70010-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70010-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70010-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70010-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70010-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="70010-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70010-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="70010-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





