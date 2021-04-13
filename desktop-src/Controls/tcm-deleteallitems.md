---
title: Message TCM_DELETEALLITEMS (commctrl. h)
description: Supprime tous les éléments d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509214"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="2f6c3-105">\_Message DELETEALLITEMS TCM</span><span class="sxs-lookup"><span data-stu-id="2f6c3-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="2f6c3-106">Supprime tous les éléments d’un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-106">Removes all items from a tab control.</span></span> <span data-ttu-id="2f6c3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="2f6c3-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f6c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f6c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f6c3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f6c3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f6c3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f6c3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f6c3-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6c3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f6c3-113">Return value</span></span>

<span data-ttu-id="2f6c3-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6c3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f6c3-115">Requirements</span></span>



| <span data-ttu-id="2f6c3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f6c3-116">Requirement</span></span> | <span data-ttu-id="2f6c3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f6c3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6c3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f6c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6c3-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f6c3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f6c3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f6c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6c3-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f6c3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f6c3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f6c3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f6c3-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6c3-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





