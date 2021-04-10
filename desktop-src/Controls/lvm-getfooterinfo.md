---
title: Message LVM_GETFOOTERINFO (commctrl. h)
description: Obtient des informations sur le pied de page d’un contrôle List-View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterInfo.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- LVM_GETFOOTERINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941675"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="1e2c9-105">\_Message GETFOOTERINFO LVM</span><span class="sxs-lookup"><span data-stu-id="1e2c9-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="1e2c9-106">Obtient des informations sur le pied de page d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="1e2c9-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="1e2c9-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e2c9-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e2c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e2c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e2c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e2c9-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e2c9-110">Not used.</span></span> <span data-ttu-id="1e2c9-111">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="1e2c9-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="1e2c9-112">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e2c9-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2c9-113">Pointeur vers une structure [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) pour recevoir des informations en fonction de la valeur du membre de **masque** .</span><span class="sxs-lookup"><span data-stu-id="1e2c9-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="1e2c9-114">Le processus appelant est responsable de l’allocation de cette structure et de la définition du membre de **masque** .</span><span class="sxs-lookup"><span data-stu-id="1e2c9-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2c9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e2c9-115">Return value</span></span>

<span data-ttu-id="1e2c9-116">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1e2c9-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2c9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e2c9-117">Requirements</span></span>



| <span data-ttu-id="1e2c9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e2c9-118">Requirement</span></span> | <span data-ttu-id="1e2c9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e2c9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2c9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2c9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e2c9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e2c9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2c9-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e2c9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e2c9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e2c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2c9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2c9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





