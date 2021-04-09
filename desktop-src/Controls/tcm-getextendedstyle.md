---
title: Message TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère les styles étendus en cours d’utilisation pour le contrôle Tab. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942699"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="76527-105">\_Message GETEXTENDEDSTYLE TCM</span><span class="sxs-lookup"><span data-stu-id="76527-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="76527-106">Récupère les styles étendus en cours d’utilisation pour le contrôle Tab.</span><span class="sxs-lookup"><span data-stu-id="76527-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="76527-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="76527-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="76527-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76527-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76527-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76527-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76527-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="76527-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76527-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76527-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76527-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="76527-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76527-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76527-113">Return value</span></span>

<span data-ttu-id="76527-114">Retourne une valeur **DWORD** qui représente les styles étendus actuellement utilisés pour le contrôle Tab.</span><span class="sxs-lookup"><span data-stu-id="76527-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="76527-115">Cette valeur est une combinaison de [styles étendus](tab-control-extended-styles.md)de contrôle d’onglet.</span><span class="sxs-lookup"><span data-stu-id="76527-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76527-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76527-116">Requirements</span></span>



| <span data-ttu-id="76527-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76527-117">Requirement</span></span> | <span data-ttu-id="76527-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="76527-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76527-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76527-119">Minimum supported client</span></span><br/> | <span data-ttu-id="76527-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76527-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76527-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76527-121">Minimum supported server</span></span><br/> | <span data-ttu-id="76527-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76527-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76527-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="76527-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="76527-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76527-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76527-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76527-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76527-126">**\_SETEXTENDEDSTYLE TCM**</span><span class="sxs-lookup"><span data-stu-id="76527-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





