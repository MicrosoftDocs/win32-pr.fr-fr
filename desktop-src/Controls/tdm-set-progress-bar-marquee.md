---
title: Message TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Démarre et arrête l’affichage du texte défilant de la barre de progression dans une boîte de dialogue de tâche et définit la vitesse du texte défilant.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033196"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="3e04b-104">\_Message de \_ \_ \_ texte défilant de la barre de progression TDM Set</span><span class="sxs-lookup"><span data-stu-id="3e04b-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="3e04b-105">Démarre et arrête l’affichage du texte défilant de la barre de progression dans une boîte de dialogue de tâche et définit la vitesse du texte défilant.</span><span class="sxs-lookup"><span data-stu-id="3e04b-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e04b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e04b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e04b-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04b-108">Valeur **booléenne** qui indique s’il faut activer ou désactiver l’affichage du texte défilant.</span><span class="sxs-lookup"><span data-stu-id="3e04b-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="3e04b-109">Utilisez **true** pour activer l’affichage du texte défilant ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="3e04b-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="3e04b-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04b-111">**Uint** qui spécifie le temps, en millisecondes, entre les mises à jour de l’animation de texte défilant.</span><span class="sxs-lookup"><span data-stu-id="3e04b-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="3e04b-112">Si ce paramètre est égal à zéro, l’animation de texte défilant est mise à jour toutes les 30 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="3e04b-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e04b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e04b-113">Return value</span></span>

<span data-ttu-id="3e04b-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3e04b-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e04b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3e04b-115">Remarks</span></span>

<span data-ttu-id="3e04b-116">Pour plus d’informations sur le mode texte défilant, consultez [contrôle de barre de progression](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="3e04b-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e04b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e04b-117">Requirements</span></span>



| <span data-ttu-id="3e04b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e04b-118">Requirement</span></span> | <span data-ttu-id="3e04b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e04b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e04b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e04b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e04b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e04b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e04b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e04b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e04b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e04b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e04b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e04b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





