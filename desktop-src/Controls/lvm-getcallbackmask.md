---
title: Message LVM_GETCALLBACKMASK (commctrl. h)
description: Obtient le masque de rappel pour un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetCallbackMask.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464282"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="bf0fc-105">\_Message GETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="bf0fc-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="bf0fc-106">Obtient le masque de rappel pour un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="bf0fc-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="bf0fc-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf0fc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf0fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf0fc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf0fc-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf0fc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf0fc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf0fc-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0fc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf0fc-113">Return value</span></span>

<span data-ttu-id="bf0fc-114">Retourne le masque de rappel.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0fc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf0fc-115">Requirements</span></span>



| <span data-ttu-id="bf0fc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf0fc-116">Requirement</span></span> | <span data-ttu-id="bf0fc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf0fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0fc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf0fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0fc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0fc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf0fc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf0fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0fc-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0fc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf0fc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf0fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0fc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0fc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





