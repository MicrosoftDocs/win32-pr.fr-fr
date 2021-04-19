---
title: RBN_AUTOSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar créé avec le \_ style RBS AutoSize quand le rebar se redimensionne automatiquement. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Contrôles Windows de code de notification RBN_AUTOSIZE
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510366"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="8463d-105">\_Code de notification de REdimensionnement automatique RBN</span><span class="sxs-lookup"><span data-stu-id="8463d-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="8463d-106">Envoyé par un contrôle rebar créé avec le style [**RBS \_ AutoSize**](rebar-control-styles.md) quand le rebar se redimensionne automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8463d-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="8463d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8463d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8463d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8463d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8463d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8463d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8463d-110">Pointeur vers une structure [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) qui contient des informations sur l’opération de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="8463d-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8463d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8463d-111">Return value</span></span>

<span data-ttu-id="8463d-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8463d-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8463d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8463d-113">Requirements</span></span>



| <span data-ttu-id="8463d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8463d-114">Requirement</span></span> | <span data-ttu-id="8463d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8463d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8463d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8463d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8463d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8463d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8463d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8463d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8463d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8463d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8463d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8463d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8463d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8463d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





