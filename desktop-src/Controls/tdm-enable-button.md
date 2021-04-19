---
title: Message TDM_ENABLE_BUTTON (commctrl. h)
description: Active ou désactive un bouton de commande dans une boîte de dialogue de tâche.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515087"
---
# <a name="tdm_enable_button-message"></a><span data-ttu-id="41146-104">Message du bouton d' \_ activation TDM \_</span><span class="sxs-lookup"><span data-stu-id="41146-104">TDM\_ENABLE\_BUTTON message</span></span>

<span data-ttu-id="41146-105">Active ou désactive un bouton de commande dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="41146-105">Enables or disables a push button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="41146-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41146-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41146-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41146-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41146-108">Valeur **int** qui spécifie l’ID du bouton de commande à activer ou à désactiver.</span><span class="sxs-lookup"><span data-stu-id="41146-108">An **int** value that specifies the ID of the push button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="41146-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41146-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41146-110">Spécifie l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="41146-110">Specifies button state.</span></span> <span data-ttu-id="41146-111">Affectez la valeur 0 pour désactiver le bouton. définissez sur une valeur différente de zéro pour activer le bouton.</span><span class="sxs-lookup"><span data-stu-id="41146-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41146-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41146-112">Return value</span></span>

<span data-ttu-id="41146-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="41146-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="41146-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41146-114">Requirements</span></span>



| <span data-ttu-id="41146-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41146-115">Requirement</span></span> | <span data-ttu-id="41146-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="41146-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41146-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41146-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41146-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41146-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41146-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41146-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41146-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41146-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41146-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="41146-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41146-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41146-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





