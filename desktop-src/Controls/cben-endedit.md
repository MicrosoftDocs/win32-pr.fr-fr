---
title: CBEN_ENDEDIT le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur a terminé une opération dans la zone d’édition ou a sélectionné un élément dans la liste déroulante du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- Contrôles Windows de code de notification CBEN_ENDEDIT
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383935"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="266d4-105">\_Code de notification CBEN ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="266d4-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="266d4-106">Envoyé lorsque l’utilisateur a terminé une opération dans la zone d’édition ou a sélectionné un élément dans la liste déroulante du contrôle.</span><span class="sxs-lookup"><span data-stu-id="266d4-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="266d4-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="266d4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="266d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="266d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="266d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="266d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="266d4-110">Pointeur vers une structure [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) qui contient des informations sur la façon dont l’utilisateur a conclu l’opération de modification.</span><span class="sxs-lookup"><span data-stu-id="266d4-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="266d4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="266d4-111">Return value</span></span>

<span data-ttu-id="266d4-112">**False** pour accepter le code de notification et autoriser le contrôle à afficher l’élément sélectionné ; Sinon, **true**.</span><span class="sxs-lookup"><span data-stu-id="266d4-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="266d4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="266d4-113">Requirements</span></span>



| <span data-ttu-id="266d4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="266d4-114">Requirement</span></span> | <span data-ttu-id="266d4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="266d4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="266d4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="266d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="266d4-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="266d4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="266d4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="266d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="266d4-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="266d4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="266d4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="266d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="266d4-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="266d4-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="266d4-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="266d4-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="266d4-123">**CBEN \_ ENDEDITW** (Unicode) et **CBEN \_ ENDEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="266d4-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="266d4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="266d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266d4-125">À propos des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="266d4-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 





