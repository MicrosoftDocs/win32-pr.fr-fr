---
title: TBN_SAVE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours d’enregistrement. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Contrôles Windows de code de notification TBN_SAVE
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743804"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="e8981-105">TBN le \_ Code de notification d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="e8981-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="e8981-106">Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e8981-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="e8981-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e8981-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e8981-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8981-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8981-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8981-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8981-110">Pointeur vers une structure [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .</span><span class="sxs-lookup"><span data-stu-id="e8981-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8981-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8981-111">Return value</span></span>

<span data-ttu-id="e8981-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e8981-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8981-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e8981-113">Remarks</span></span>

<span data-ttu-id="e8981-114">L’application recevra ce code de notification une fois au début du processus d’enregistrement et une fois pour chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="e8981-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="e8981-115">Ce code de notification vous donne la possibilité d’ajouter vos propres informations à celles enregistrées par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e8981-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="e8981-116">Si vous ne souhaitez pas ajouter d’informations, ignorez le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e8981-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="e8981-117">Pour plus d’informations sur la gestion de TBN, consultez Personnalisation de la [barre d’outils](toolbar-controls-overview.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="e8981-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8981-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8981-118">Requirements</span></span>



| <span data-ttu-id="e8981-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8981-119">Requirement</span></span> | <span data-ttu-id="e8981-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8981-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8981-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8981-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8981-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8981-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8981-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8981-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8981-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8981-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8981-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8981-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8981-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8981-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8981-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8981-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8981-128">\_restauration TBN</span><span class="sxs-lookup"><span data-stu-id="e8981-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





