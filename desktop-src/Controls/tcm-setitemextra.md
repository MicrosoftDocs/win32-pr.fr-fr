---
title: Message TCM_SETITEMEXTRA (commctrl. h)
description: Définit le nombre d’octets par onglet réservé pour les données définies par l’application dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102856"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="0a60c-105">\_Message SETITEMEXTRA TCM</span><span class="sxs-lookup"><span data-stu-id="0a60c-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="0a60c-106">Définit le nombre d’octets par onglet réservé pour les données définies par l’application dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="0a60c-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="0a60c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .</span><span class="sxs-lookup"><span data-stu-id="0a60c-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a60c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a60c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a60c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a60c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a60c-110">Nombre d’octets supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0a60c-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0a60c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a60c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a60c-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0a60c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a60c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a60c-113">Return value</span></span>

<span data-ttu-id="0a60c-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0a60c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a60c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0a60c-115">Remarks</span></span>

<span data-ttu-id="0a60c-116">Par défaut, le nombre d’octets supplémentaires est de quatre.</span><span class="sxs-lookup"><span data-stu-id="0a60c-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="0a60c-117">Une application qui modifie le nombre d’octets supplémentaires ne peut pas utiliser la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) pour récupérer et définir les données définies par l’application pour un onglet. Au lieu de cela, vous devez définir une nouvelle structure qui se compose de la structure [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) suivie de membres définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0a60c-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="0a60c-118">Une application doit uniquement modifier le nombre d’octets en trop lorsqu’un contrôle onglet ne contient pas d’onglets.</span><span class="sxs-lookup"><span data-stu-id="0a60c-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a60c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a60c-119">Requirements</span></span>



| <span data-ttu-id="0a60c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a60c-120">Requirement</span></span> | <span data-ttu-id="0a60c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a60c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a60c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a60c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a60c-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a60c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a60c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a60c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a60c-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a60c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a60c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a60c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a60c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a60c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





