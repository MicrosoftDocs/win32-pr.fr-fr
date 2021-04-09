---
title: Message LVM_GETFOOTERITEM (commctrl. h)
description: Obtient des informations sur un élément de pied de page dans un contrôle List-View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032352"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="5dde9-105">\_Message GETFOOTERITEM LVM</span><span class="sxs-lookup"><span data-stu-id="5dde9-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="5dde9-106">Obtient des informations sur un élément de pied de page dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="5dde9-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="5dde9-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .</span><span class="sxs-lookup"><span data-stu-id="5dde9-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dde9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dde9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dde9-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5dde9-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dde9-110">Index de l'élément.</span><span class="sxs-lookup"><span data-stu-id="5dde9-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="5dde9-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5dde9-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dde9-112">Pointeur vers une structure [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) pour recevoir une valeur pour l' **État** et/ou les membres **pszText** en fonction de la valeur du membre de **masque** .</span><span class="sxs-lookup"><span data-stu-id="5dde9-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="5dde9-113">Le processus appelant est chargé d’allouer cette structure et de définir ses membres pour indiquer au destinataire les informations à retourner.</span><span class="sxs-lookup"><span data-stu-id="5dde9-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="5dde9-114">Pour plus d’informations, consultez **LVFOOTERITEM**.</span><span class="sxs-lookup"><span data-stu-id="5dde9-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dde9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5dde9-115">Return value</span></span>

<span data-ttu-id="5dde9-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5dde9-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dde9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dde9-117">Requirements</span></span>



| <span data-ttu-id="5dde9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dde9-118">Requirement</span></span> | <span data-ttu-id="5dde9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dde9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dde9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dde9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5dde9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dde9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5dde9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dde9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5dde9-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dde9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dde9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5dde9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dde9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dde9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





