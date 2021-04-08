---
title: Message LVM_GETITEMCOUNT (commctrl. h)
description: Récupère le nombre d’éléments dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemCount.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742989"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="6b8b0-105">\_Message GETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="6b8b0-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="6b8b0-106">Récupère le nombre d’éléments dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="6b8b0-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="6b8b0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="6b8b0-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b8b0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b8b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b8b0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6b8b0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6b8b0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6b8b0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b8b0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6b8b0-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6b8b0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8b0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b8b0-113">Return value</span></span>

<span data-ttu-id="6b8b0-114">Retourne le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="6b8b0-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8b0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b8b0-115">Requirements</span></span>



| <span data-ttu-id="6b8b0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b8b0-116">Requirement</span></span> | <span data-ttu-id="6b8b0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b8b0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8b0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b8b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8b0-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b8b0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b8b0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b8b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8b0-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b8b0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b8b0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b8b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8b0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8b0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





