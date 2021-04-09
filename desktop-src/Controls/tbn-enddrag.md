---
title: TBN_ENDDRAG le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils que l’utilisateur a cessé de faire glisser un bouton dans une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- Contrôles Windows de code de notification TBN_ENDDRAG
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105031"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="4050f-105">\_Code de notification TBN ENDDRAG</span><span class="sxs-lookup"><span data-stu-id="4050f-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="4050f-106">Avertit la fenêtre parente de la barre d’outils que l’utilisateur a cessé de faire glisser un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4050f-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="4050f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4050f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4050f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4050f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4050f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4050f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4050f-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="4050f-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="4050f-111">Le membre **iItem** contient l’identificateur de commande du bouton qui est glissé.</span><span class="sxs-lookup"><span data-stu-id="4050f-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4050f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4050f-112">Return value</span></span>

<span data-ttu-id="4050f-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4050f-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4050f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4050f-114">Requirements</span></span>



| <span data-ttu-id="4050f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4050f-115">Requirement</span></span> | <span data-ttu-id="4050f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4050f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4050f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4050f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4050f-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4050f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4050f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4050f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4050f-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4050f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4050f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4050f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4050f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4050f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





