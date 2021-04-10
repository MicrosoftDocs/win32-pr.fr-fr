---
title: Message EM_ENABLESEARCHWEB (CommCtrl. h)
description: Active ou désactive la fonctionnalité « Rechercher sur le Web » et l’entrée du menu contextuel.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942386"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="bb5eb-104">\_Message ENABLESEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="bb5eb-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="bb5eb-105">Active ou désactive la fonctionnalité « Rechercher sur le Web » et l’entrée du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="bb5eb-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb5eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb5eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb5eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5eb-108">La valeur **true** indique que la fonctionnalité « Rechercher sur le Web » est activée, et la valeur **false** indique qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="bb5eb-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="bb5eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb5eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5eb-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="bb5eb-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5eb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb5eb-111">Return value</span></span>

<span data-ttu-id="bb5eb-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bb5eb-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5eb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bb5eb-113">Remarks</span></span>

<span data-ttu-id="bb5eb-114">Si vous désactivez « Rechercher sur le Web » à l’aide de ce message, le message [**em \_ SEARCHWEB**](em-searchweb.md) n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="bb5eb-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5eb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb5eb-115">Requirements</span></span>



| <span data-ttu-id="bb5eb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb5eb-116">Requirement</span></span> | <span data-ttu-id="bb5eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb5eb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5eb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb5eb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb5eb-119">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb5eb-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb5eb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb5eb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb5eb-121">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb5eb-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb5eb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb5eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb5eb-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5eb-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb5eb-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb5eb-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bb5eb-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb5eb-126">**\_SEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="bb5eb-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 





