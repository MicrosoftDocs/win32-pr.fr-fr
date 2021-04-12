---
title: Message LVM_GETHOTITEM (commctrl. h)
description: Récupère l’index de l’élément réactif. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHotItem.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105514"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="12f4a-105">\_Message GETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="12f4a-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="12f4a-106">Récupère l’index de l’élément réactif.</span><span class="sxs-lookup"><span data-stu-id="12f4a-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="12f4a-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .</span><span class="sxs-lookup"><span data-stu-id="12f4a-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="12f4a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12f4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f4a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12f4a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12f4a-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="12f4a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="12f4a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12f4a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="12f4a-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="12f4a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f4a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12f4a-113">Return value</span></span>

<span data-ttu-id="12f4a-114">Retourne l’index de l’élément qui est actif.</span><span class="sxs-lookup"><span data-stu-id="12f4a-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f4a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12f4a-115">Requirements</span></span>



| <span data-ttu-id="12f4a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12f4a-116">Requirement</span></span> | <span data-ttu-id="12f4a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="12f4a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12f4a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f4a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12f4a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12f4a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12f4a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f4a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12f4a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12f4a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12f4a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="12f4a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f4a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f4a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





