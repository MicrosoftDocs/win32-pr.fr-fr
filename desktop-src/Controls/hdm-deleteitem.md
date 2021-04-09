---
title: Message HDM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser l’en-tête de la \_ macro DeleteItem.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033017"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="622df-105">\_Message HDM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="622df-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="622df-106">Supprime un élément d’un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="622df-106">Deletes an item from a header control.</span></span> <span data-ttu-id="622df-107">Vous pouvez envoyer ce message explicitement ou utiliser l' [**en \_ -tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) de la macro DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="622df-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="622df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="622df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="622df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="622df-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="622df-110">Index de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="622df-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="622df-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="622df-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="622df-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="622df-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="622df-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="622df-113">Return value</span></span>

<span data-ttu-id="622df-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="622df-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="622df-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="622df-115">Requirements</span></span>



| <span data-ttu-id="622df-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="622df-116">Requirement</span></span> | <span data-ttu-id="622df-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="622df-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="622df-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="622df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="622df-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="622df-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="622df-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="622df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="622df-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="622df-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="622df-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="622df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="622df-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="622df-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





