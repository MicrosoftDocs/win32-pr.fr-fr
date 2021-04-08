---
title: Message TCM_GETROWCOUNT (commctrl. h)
description: Récupère le nombre actuel de lignes d’onglets dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844178"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="66a51-105">\_Message GETROWCOUNT de TCM</span><span class="sxs-lookup"><span data-stu-id="66a51-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="66a51-106">Récupère le nombre actuel de lignes d’onglets dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="66a51-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="66a51-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .</span><span class="sxs-lookup"><span data-stu-id="66a51-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66a51-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66a51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a51-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66a51-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="66a51-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="66a51-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="66a51-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66a51-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="66a51-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="66a51-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a51-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66a51-113">Return value</span></span>

<span data-ttu-id="66a51-114">Retourne le nombre de lignes d’onglets.</span><span class="sxs-lookup"><span data-stu-id="66a51-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a51-115">Notes</span><span class="sxs-lookup"><span data-stu-id="66a51-115">Remarks</span></span>

<span data-ttu-id="66a51-116">Seuls les contrôles onglet avec le [**style \_ multiligne TCS**](tab-control-styles.md) peuvent avoir plusieurs lignes d’onglets.</span><span class="sxs-lookup"><span data-stu-id="66a51-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a51-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66a51-117">Requirements</span></span>



| <span data-ttu-id="66a51-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66a51-118">Requirement</span></span> | <span data-ttu-id="66a51-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="66a51-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66a51-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66a51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66a51-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66a51-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66a51-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66a51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66a51-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66a51-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66a51-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="66a51-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a51-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a51-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





