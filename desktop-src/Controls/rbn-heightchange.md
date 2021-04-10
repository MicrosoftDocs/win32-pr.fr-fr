---
title: RBN_HEIGHTCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque sa hauteur a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- Contrôles Windows de code de notification RBN_HEIGHTCHANGE
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942066"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="85214-105">\_Code de notification RBN HEIGHTCHANGE</span><span class="sxs-lookup"><span data-stu-id="85214-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="85214-106">Envoyé par un contrôle rebar lorsque sa hauteur a changé.</span><span class="sxs-lookup"><span data-stu-id="85214-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="85214-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="85214-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="85214-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85214-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85214-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85214-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85214-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="85214-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85214-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85214-111">Return value</span></span>

<span data-ttu-id="85214-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="85214-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="85214-113">Notes</span><span class="sxs-lookup"><span data-stu-id="85214-113">Remarks</span></span>

<span data-ttu-id="85214-114">Les contrôles Rebar qui utilisent le style [**CCS \_ vert**](common-control-styles.md) envoient ce code de notification lorsque leur largeur change.</span><span class="sxs-lookup"><span data-stu-id="85214-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="85214-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85214-115">Requirements</span></span>



| <span data-ttu-id="85214-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85214-116">Requirement</span></span> | <span data-ttu-id="85214-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="85214-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85214-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85214-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85214-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85214-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85214-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85214-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85214-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85214-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85214-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="85214-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85214-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85214-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





