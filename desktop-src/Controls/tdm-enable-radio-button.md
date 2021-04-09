---
title: Message TDM_ENABLE_RADIO_BUTTON (commctrl. h)
description: Active ou désactive une case d’option dans une boîte de dialogue de tâche.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942758"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="e6e25-104">Message d’activation de la \_ \_ case d’option TDM \_</span><span class="sxs-lookup"><span data-stu-id="e6e25-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="e6e25-105">Active ou désactive une case d’option dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="e6e25-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6e25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6e25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e25-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e25-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e25-108">Valeur **int** qui spécifie l’ID de la case d’option à activer ou à désactiver.</span><span class="sxs-lookup"><span data-stu-id="e6e25-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e6e25-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6e25-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e25-110">Spécifie l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="e6e25-110">Specifies button state.</span></span> <span data-ttu-id="e6e25-111">Affectez la valeur 0 pour désactiver le bouton. définissez sur une valeur différente de zéro pour activer le bouton.</span><span class="sxs-lookup"><span data-stu-id="e6e25-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e25-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6e25-112">Return value</span></span>

<span data-ttu-id="e6e25-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e6e25-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e25-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6e25-114">Requirements</span></span>



| <span data-ttu-id="e6e25-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6e25-115">Requirement</span></span> | <span data-ttu-id="e6e25-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6e25-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e25-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6e25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e25-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6e25-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6e25-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6e25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e25-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6e25-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6e25-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6e25-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e25-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e25-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





