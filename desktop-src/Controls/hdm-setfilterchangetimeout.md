---
title: Message HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Définit l’intervalle de délai d’attente entre le moment où une modification est effectuée dans les attributs de filtre et la publication d’une \_ notification HDN FILTERCHANGE. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033109"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="a9ec8-105">\_Message HDM SETFILTERCHANGETIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a9ec8-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="a9ec8-106">Définit l’intervalle de délai d’attente entre le moment où une modification est effectuée dans les attributs de filtre et la publication d’une notification [HDN \_ FILTERCHANGE](hdn-filterchange.md) .</span><span class="sxs-lookup"><span data-stu-id="a9ec8-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="a9ec8-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .</span><span class="sxs-lookup"><span data-stu-id="a9ec8-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9ec8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9ec8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ec8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9ec8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a9ec8-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a9ec8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a9ec8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9ec8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ec8-112">Valeur du délai d'attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a9ec8-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ec8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9ec8-113">Return value</span></span>

<span data-ttu-id="a9ec8-114">Retourne l’index du contrôle de filtre en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="a9ec8-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ec8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9ec8-115">Requirements</span></span>



| <span data-ttu-id="a9ec8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9ec8-116">Requirement</span></span> | <span data-ttu-id="a9ec8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9ec8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ec8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9ec8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ec8-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9ec8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9ec8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9ec8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ec8-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9ec8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9ec8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9ec8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ec8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ec8-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ec8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9ec8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ec8-125">HDN \_ FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="a9ec8-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





