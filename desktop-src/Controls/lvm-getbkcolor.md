---
title: Message LVM_GETBKCOLOR (commctrl. h)
description: Obtient la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetBkColor.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- LVM_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464286"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="cdcd9-105">\_Message GETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="cdcd9-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="cdcd9-106">Obtient la couleur d’arrière-plan d’un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="cdcd9-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="cdcd9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="cdcd9-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdcd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdcd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdcd9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdcd9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cdcd9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cdcd9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cdcd9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdcd9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cdcd9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cdcd9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdcd9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdcd9-113">Return value</span></span>

<span data-ttu-id="cdcd9-114">Retourne la couleur d’arrière-plan du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="cdcd9-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcd9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdcd9-115">Requirements</span></span>



| <span data-ttu-id="cdcd9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdcd9-116">Requirement</span></span> | <span data-ttu-id="cdcd9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdcd9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcd9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdcd9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcd9-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdcd9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdcd9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdcd9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcd9-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdcd9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cdcd9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdcd9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdcd9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdcd9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





