---
title: Message TCM_SETMINTABWIDTH (commctrl. h)
description: Définit la largeur minimale des éléments dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518056"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="1c796-105">\_Message SETMINTABWIDTH TCM</span><span class="sxs-lookup"><span data-stu-id="1c796-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="1c796-106">Définit la largeur minimale des éléments dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="1c796-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="1c796-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .</span><span class="sxs-lookup"><span data-stu-id="1c796-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c796-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c796-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c796-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c796-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1c796-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1c796-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1c796-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c796-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c796-112">Largeur minimale à définir pour un élément de contrôle d’onglet.</span><span class="sxs-lookup"><span data-stu-id="1c796-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="1c796-113">Si ce paramètre a la valeur-1, le contrôle utilise la largeur d’onglet par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c796-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c796-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c796-114">Return value</span></span>

<span data-ttu-id="1c796-115">Retourne une valeur INT qui représente la largeur d’onglet minimale précédente.</span><span class="sxs-lookup"><span data-stu-id="1c796-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c796-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c796-116">Requirements</span></span>



| <span data-ttu-id="1c796-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c796-117">Requirement</span></span> | <span data-ttu-id="1c796-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c796-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c796-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c796-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c796-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c796-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c796-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c796-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c796-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c796-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c796-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c796-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c796-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c796-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





