---
title: Message CCM_DPISCALE (commctrl. h)
description: Active la mise à l’échelle en points par pouce (dpi) automatique dans les contrôles de Tree-View, les contrôles de List-View, les contrôles ComboBoxEx, les contrôles d’en-tête, les boutons, les contrôles ToolBar, les contrôles d’animation et les listes d’images.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104518"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="56ee0-104">\_Message CCM DPISCALE</span><span class="sxs-lookup"><span data-stu-id="56ee0-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="56ee0-105">Active la mise à l’échelle en points par pouce (dpi) automatique dans [les contrôles d’affichage d’arborescence](tree-view-controls.md), [les contrôles de vue de liste](list-view-control-reference.md), les [contrôles ComboBoxEx](comboboxex-controls.md), les [contrôles d’en-tête](header-controls.md), les [boutons](buttons.md), les [contrôles ToolBar](toolbar-controls-overview.md), les [contrôles d’animation](animation-control-overview.md)et les [listes d’images](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="56ee0-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="56ee0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56ee0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ee0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56ee0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56ee0-108">Affectez la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="56ee0-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="56ee0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56ee0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56ee0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="56ee0-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ee0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56ee0-111">Return value</span></span>

<span data-ttu-id="56ee0-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="56ee0-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ee0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="56ee0-113">Remarks</span></span>

<span data-ttu-id="56ee0-114">Le lancement rapide et la [barre des tâches](/windows/desktop/shell/taskbar) ne doivent pas spécifier de mise à l’échelle dpi, car les images sont déjà mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="56ee0-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="56ee0-115">Tout contrôle qui utilise une liste d’images créée avec la métrique SmallIcon ne doit pas mettre à l’échelle ses icônes.</span><span class="sxs-lookup"><span data-stu-id="56ee0-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="56ee0-116">Pour utiliser cette API, vous devez fournir un manifeste qui spécifie Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="56ee0-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="56ee0-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="56ee0-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56ee0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56ee0-118">Requirements</span></span>



| <span data-ttu-id="56ee0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56ee0-119">Requirement</span></span> | <span data-ttu-id="56ee0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="56ee0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56ee0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ee0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56ee0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ee0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56ee0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56ee0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56ee0-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56ee0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56ee0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="56ee0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ee0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ee0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

