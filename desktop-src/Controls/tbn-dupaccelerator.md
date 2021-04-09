---
title: TBN_DUPACCELERATOR le code de notification (commctrl. h)
description: Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Contrôles Windows de code de notification TBN_DUPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033089"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="eeaf4-105">\_Code de notification TBN DUPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="eeaf4-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="eeaf4-106">Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="eeaf4-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eeaf4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eeaf4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eeaf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeaf4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeaf4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeaf4-110">Pointeur vers une structure qui fournit un accélérateur et qui reçoit une valeur spécifiant si plusieurs barres d’outils répondent au même caractère.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeaf4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eeaf4-111">Return value</span></span>

<span data-ttu-id="eeaf4-112">Retourne la **valeur true** en cas de réussite, sinon **false**.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeaf4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eeaf4-113">Remarks</span></span>

<span data-ttu-id="eeaf4-114">L’application doit déclarer la structure **NMTBDUPACCELERATOR** comme suit :</span><span class="sxs-lookup"><span data-stu-id="eeaf4-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="eeaf4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeaf4-115">Requirements</span></span>



| <span data-ttu-id="eeaf4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeaf4-116">Requirement</span></span> | <span data-ttu-id="eeaf4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeaf4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeaf4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeaf4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eeaf4-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeaf4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeaf4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeaf4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eeaf4-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeaf4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eeaf4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeaf4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeaf4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeaf4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





