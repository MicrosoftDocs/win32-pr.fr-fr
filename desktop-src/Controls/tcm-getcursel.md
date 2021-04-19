---
title: Message TCM_GETCURSEL (commctrl. h)
description: Détermine l’onglet actuellement sélectionné dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513630"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="32e84-105">\_Message GETCURSEL TCM</span><span class="sxs-lookup"><span data-stu-id="32e84-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="32e84-106">Détermine l’onglet actuellement sélectionné dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="32e84-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="32e84-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="32e84-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="32e84-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32e84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32e84-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32e84-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="32e84-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32e84-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32e84-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32e84-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="32e84-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e84-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32e84-113">Return value</span></span>

<span data-ttu-id="32e84-114">Retourne l’index de l’onglet sélectionné en cas de réussite, ou-1 si aucun onglet n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="32e84-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e84-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32e84-115">Requirements</span></span>



| <span data-ttu-id="32e84-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e84-116">Requirement</span></span> | <span data-ttu-id="32e84-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e84-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32e84-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e84-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32e84-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e84-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32e84-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e84-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32e84-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e84-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32e84-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="32e84-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e84-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e84-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





