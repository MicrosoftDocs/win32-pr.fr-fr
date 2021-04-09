---
title: Message LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcule la largeur et la hauteur approximatives requises pour afficher un nombre donné d’éléments. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView ApproximateViewRect.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941679"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="f29ec-105">\_Message APPROXIMATEVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="f29ec-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="f29ec-106">Calcule la largeur et la hauteur approximatives requises pour afficher un nombre donné d’éléments.</span><span class="sxs-lookup"><span data-stu-id="f29ec-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="f29ec-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .</span><span class="sxs-lookup"><span data-stu-id="f29ec-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f29ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f29ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f29ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f29ec-110">Nombre d’éléments à afficher dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f29ec-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="f29ec-111">Si ce paramètre a la valeur-1, le message utilise le nombre total d’éléments dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f29ec-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="f29ec-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f29ec-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f29ec-113">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la dimension x proposée du contrôle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f29ec-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="f29ec-114">Ce paramètre peut être défini sur-1 pour permettre au message d’utiliser la valeur de largeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="f29ec-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="f29ec-115">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est la dimension y proposée du contrôle, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f29ec-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="f29ec-116">Ce paramètre peut être défini sur-1 pour permettre au message d’utiliser la valeur de la hauteur actuelle.</span><span class="sxs-lookup"><span data-stu-id="f29ec-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29ec-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f29ec-117">Return value</span></span>

<span data-ttu-id="f29ec-118">Retourne une valeur **DWORD** qui contient la largeur approximative (dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) et la hauteur (dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) nécessaire pour afficher les éléments, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f29ec-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="f29ec-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f29ec-119">Remarks</span></span>

<span data-ttu-id="f29ec-120">La définition de la taille du contrôle d’affichage de liste en fonction des dimensions fournies par ce message peut optimiser le scintillement et réduire le scintillement.</span><span class="sxs-lookup"><span data-stu-id="f29ec-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="f29ec-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f29ec-121">Requirements</span></span>



| <span data-ttu-id="f29ec-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f29ec-122">Requirement</span></span> | <span data-ttu-id="f29ec-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f29ec-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f29ec-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f29ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f29ec-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f29ec-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f29ec-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f29ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f29ec-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f29ec-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f29ec-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f29ec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29ec-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29ec-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

