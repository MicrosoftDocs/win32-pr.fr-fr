---
title: Message LVM_SETHOTCURSOR (commctrl. h)
description: Définit la valeur HCURSOR utilisée par le contrôle List-View lorsque le pointeur se trouve sur un élément alors que la sélection active est activée.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739948"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="39760-104">\_Message SETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="39760-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="39760-105">Définit la valeur HCURSOR utilisée par le contrôle List-View lorsque le pointeur se trouve sur un élément alors que la sélection active est activée.</span><span class="sxs-lookup"><span data-stu-id="39760-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="39760-106">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="39760-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="39760-107">Pour vérifier si la surveillance à chaud est activée, appelez [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="39760-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="39760-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39760-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39760-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39760-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39760-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="39760-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="39760-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39760-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39760-112">Handle du curseur à définir.</span><span class="sxs-lookup"><span data-stu-id="39760-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39760-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39760-113">Return value</span></span>

<span data-ttu-id="39760-114">Retourne une valeur HCURSOR qui est le curseur réactif précédent.</span><span class="sxs-lookup"><span data-stu-id="39760-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="39760-115">Notes</span><span class="sxs-lookup"><span data-stu-id="39760-115">Remarks</span></span>

<span data-ttu-id="39760-116">Un contrôle List-View utilise le suivi réactif et la sélection au pointage lorsque le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="39760-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="39760-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39760-117">Requirements</span></span>



| <span data-ttu-id="39760-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39760-118">Requirement</span></span> | <span data-ttu-id="39760-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="39760-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39760-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39760-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39760-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39760-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39760-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39760-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39760-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39760-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39760-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="39760-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39760-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39760-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

