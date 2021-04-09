---
title: TBN_ENDADJUST le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a arrêté de personnaliser une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- Contrôles Windows de code de notification TBN_ENDADJUST
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032750"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="bfd5c-105">\_Code de notification TBN ENDADJUST</span><span class="sxs-lookup"><span data-stu-id="bfd5c-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="bfd5c-106">Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a arrêté de personnaliser une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bfd5c-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="bfd5c-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd5c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bfd5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfd5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfd5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfd5c-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="bfd5c-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd5c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfd5c-111">Return value</span></span>

<span data-ttu-id="bfd5c-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bfd5c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd5c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfd5c-113">Requirements</span></span>



| <span data-ttu-id="bfd5c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfd5c-114">Requirement</span></span> | <span data-ttu-id="bfd5c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd5c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd5c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd5c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd5c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfd5c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfd5c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd5c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd5c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfd5c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfd5c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfd5c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd5c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd5c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





