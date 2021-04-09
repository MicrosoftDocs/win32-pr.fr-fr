---
title: TBN_BEGINDRAG le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à faire glisser un bouton dans une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- Contrôles Windows de code de notification TBN_BEGINDRAG
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103217"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="4b3dd-105">\_Code de notification TBN BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="4b3dd-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="4b3dd-106">Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à faire glisser un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4b3dd-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="4b3dd-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4b3dd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4b3dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b3dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b3dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b3dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b3dd-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="4b3dd-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="4b3dd-111">Le membre **iItem** contient l’identificateur de commande du bouton qui est glissé.</span><span class="sxs-lookup"><span data-stu-id="4b3dd-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b3dd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b3dd-112">Return value</span></span>

<span data-ttu-id="4b3dd-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4b3dd-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3dd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b3dd-114">Requirements</span></span>



| <span data-ttu-id="4b3dd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b3dd-115">Requirement</span></span> | <span data-ttu-id="4b3dd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b3dd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3dd-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3dd-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b3dd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b3dd-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3dd-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b3dd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b3dd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b3dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b3dd-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b3dd-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





