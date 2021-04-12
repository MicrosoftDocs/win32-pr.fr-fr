---
title: Message BCM_GETIMAGELIST (commctrl. h)
description: Obtient la \_ structure IMAGELIST du bouton qui décrit la liste d’images assignée à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetImageList macro.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465494"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="7d6cc-105">\_Message GETIMAGELIST BCM</span><span class="sxs-lookup"><span data-stu-id="7d6cc-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="7d6cc-106">Obtient la [**structure \_ IMAGELIST du bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui décrit la liste d’images assignée à un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="7d6cc-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d6cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d6cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d6cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6cc-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d6cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d6cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6cc-112">Pointeur vers une structure [**\_ IMAGELIST de bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui contient des informations sur la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6cc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d6cc-113">Return value</span></span>

<span data-ttu-id="7d6cc-114">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="7d6cc-115">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6cc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7d6cc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7d6cc-117">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="7d6cc-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7d6cc-118">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7d6cc-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d6cc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d6cc-119">Requirements</span></span>



| <span data-ttu-id="7d6cc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d6cc-120">Requirement</span></span> | <span data-ttu-id="7d6cc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d6cc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6cc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d6cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d6cc-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d6cc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d6cc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d6cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d6cc-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d6cc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d6cc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d6cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d6cc-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6cc-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





