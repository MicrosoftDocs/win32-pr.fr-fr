---
title: TBN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle ToolBar qui utilise le \_ style TBSTYLE REGISTERDROP pour demander un objet cible de déplacement lorsque le pointeur passe sur l’un de ses boutons. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Contrôles Windows de code de notification TBN_GETOBJECT
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102860"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="165cc-105">\_Code de notification TBN GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="165cc-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="165cc-106">Envoyé par un contrôle ToolBar qui utilise le style [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) pour demander un objet cible de déplacement lorsque le pointeur passe sur l’un de ses boutons.</span><span class="sxs-lookup"><span data-stu-id="165cc-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="165cc-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="165cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="165cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="165cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="165cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="165cc-110">Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur le bouton sur lequel le pointeur a passé et reçoit les données fournies par l’application en réponse à ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="165cc-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165cc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="165cc-111">Return value</span></span>

<span data-ttu-id="165cc-112">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="165cc-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="165cc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="165cc-113">Remarks</span></span>

<span data-ttu-id="165cc-114">Pour fournir un objet, une application doit définir des valeurs dans certains membres de la structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) au niveau de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="165cc-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="165cc-115">Le membre **pObject** doit être défini sur un pointeur d’objet valide et le membre **HRESULT** doit être défini sur un indicateur de réussite.</span><span class="sxs-lookup"><span data-stu-id="165cc-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="165cc-116">Pour se conformer aux normes COM (Component Object Model), incrémentez toujours le nombre de références de l’objet lors de la fourniture d’un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="165cc-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="165cc-117">Si une application ne fournit pas d’objet, elle doit affecter la valeur **null** à **pObject** et **HRESULT** à un indicateur d’échec.</span><span class="sxs-lookup"><span data-stu-id="165cc-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="165cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="165cc-118">Requirements</span></span>



| <span data-ttu-id="165cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="165cc-119">Requirement</span></span> | <span data-ttu-id="165cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="165cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="165cc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="165cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="165cc-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="165cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="165cc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="165cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="165cc-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="165cc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="165cc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="165cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="165cc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="165cc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





