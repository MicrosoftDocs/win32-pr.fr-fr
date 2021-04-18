---
title: Message LVM_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte d’un contrôle List View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTextColor.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- LVM_GETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533573"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="87d39-105">\_Message GETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="87d39-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="87d39-106">Récupère la couleur de texte d’un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="87d39-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="87d39-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="87d39-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87d39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87d39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87d39-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87d39-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="87d39-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="87d39-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87d39-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87d39-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="87d39-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d39-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87d39-113">Return value</span></span>

<span data-ttu-id="87d39-114">Retourne la couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="87d39-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d39-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87d39-115">Requirements</span></span>



| <span data-ttu-id="87d39-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87d39-116">Requirement</span></span> | <span data-ttu-id="87d39-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="87d39-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87d39-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87d39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87d39-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87d39-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87d39-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87d39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87d39-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87d39-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87d39-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="87d39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d39-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87d39-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





