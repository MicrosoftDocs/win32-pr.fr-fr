---
title: Message TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Spécifie si un lien de commande ou un bouton de boîte de dialogue de tâche donné doit avoir une icône de protection de contrôle de compte d’utilisateur (UAC). autrement dit, si l’action appelée par le bouton requiert une élévation.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105973"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="3e9e2-104">Message d’état d’élévation de bouton de l' \_ ensemble TDM \_ \_ \_ requis \_</span><span class="sxs-lookup"><span data-stu-id="3e9e2-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="3e9e2-105">Spécifie si un lien de commande ou un bouton de boîte de dialogue de tâche donné doit avoir une icône de protection de contrôle de compte d’utilisateur (UAC). autrement dit, si l’action appelée par le bouton requiert une élévation.</span><span class="sxs-lookup"><span data-stu-id="3e9e2-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e9e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e9e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9e2-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e9e2-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9e2-108">ID du bouton de commande ou du lien de commande à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="3e9e2-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="3e9e2-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e9e2-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9e2-110">Affectez la valeur 0 pour indiquer que l’action appelée par le bouton ne requiert pas d’élévation.</span><span class="sxs-lookup"><span data-stu-id="3e9e2-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="3e9e2-111">Définissez sur une valeur différente de zéro pour indiquer que l’action requiert une élévation.</span><span class="sxs-lookup"><span data-stu-id="3e9e2-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9e2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e9e2-112">Return value</span></span>

<span data-ttu-id="3e9e2-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3e9e2-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9e2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e9e2-114">Requirements</span></span>



| <span data-ttu-id="3e9e2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e9e2-115">Requirement</span></span> | <span data-ttu-id="3e9e2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e9e2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9e2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e9e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9e2-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e9e2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e9e2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e9e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9e2-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e9e2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e9e2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e9e2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9e2-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





