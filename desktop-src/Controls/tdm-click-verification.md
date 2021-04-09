---
title: Message TDM_CLICK_VERIFICATION (commctrl. h)
description: Simule un clic de la case à cocher vérification d’une boîte de dialogue de tâche, si elle existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102852"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="6771b-104">Message de vérification de \_ clic TDM \_</span><span class="sxs-lookup"><span data-stu-id="6771b-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="6771b-105">Simule un clic de la case à cocher vérification d’une boîte de dialogue de tâche, si elle existe.</span><span class="sxs-lookup"><span data-stu-id="6771b-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="6771b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6771b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6771b-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6771b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6771b-108">**True** pour définir l’état de la case à cocher à vérifier ; **False** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="6771b-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="6771b-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6771b-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6771b-110">**True** pour définir le focus clavier sur la case à cocher ; **False** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6771b-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6771b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6771b-111">Return value</span></span>

<span data-ttu-id="6771b-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6771b-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6771b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6771b-113">Requirements</span></span>



| <span data-ttu-id="6771b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6771b-114">Requirement</span></span> | <span data-ttu-id="6771b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6771b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6771b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6771b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6771b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6771b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6771b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6771b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6771b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6771b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6771b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6771b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6771b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6771b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





