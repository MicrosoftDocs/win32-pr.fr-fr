---
title: Message LVM_GETHEADER (commctrl. h)
description: Obtient le handle du contrôle d’en-tête utilisé par le contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032428"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="95fb5-105">\_Message GETHEADER LVM</span><span class="sxs-lookup"><span data-stu-id="95fb5-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="95fb5-106">Obtient le handle du contrôle d’en-tête utilisé par le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="95fb5-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="95fb5-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .</span><span class="sxs-lookup"><span data-stu-id="95fb5-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95fb5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95fb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fb5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95fb5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="95fb5-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95fb5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="95fb5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95fb5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95fb5-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95fb5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fb5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95fb5-113">Return value</span></span>

<span data-ttu-id="95fb5-114">Retourne le handle du contrôle header.</span><span class="sxs-lookup"><span data-stu-id="95fb5-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fb5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95fb5-115">Requirements</span></span>



| <span data-ttu-id="95fb5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95fb5-116">Requirement</span></span> | <span data-ttu-id="95fb5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="95fb5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95fb5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95fb5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="95fb5-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95fb5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95fb5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95fb5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="95fb5-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95fb5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95fb5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="95fb5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="95fb5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95fb5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





