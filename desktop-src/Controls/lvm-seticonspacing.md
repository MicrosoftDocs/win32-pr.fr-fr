---
title: Message LVM_SETICONSPACING (commctrl. h)
description: Définit l’espacement entre les icônes des contrôles d’affichage de liste qui ont le \_ style d’icône LVS. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetIconSpacing.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843093"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="3fcdb-105">\_Message SETICONSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="3fcdb-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="3fcdb-106">Définit l’espacement entre les icônes des contrôles d’affichage de liste qui ont le style d' [**\_ icône LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3fcdb-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="3fcdb-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .</span><span class="sxs-lookup"><span data-stu-id="3fcdb-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fcdb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fcdb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fcdb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fcdb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcdb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3fcdb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fcdb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcdb-112">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la distance, en pixels, à définir entre les icônes sur l’axe des abscisses.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="3fcdb-113">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la distance, en pixels, à définir entre les icônes sur l’axe des ordonnées.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="3fcdb-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fcdb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fcdb-115">Return value</span></span>

<span data-ttu-id="3fcdb-116">Retourne une valeur **DWORD** qui contient la distance précédente de l’axe x dans le mot bas, et la distance de l’axe y précédente dans le mot haut.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fcdb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3fcdb-117">Remarks</span></span>

<span data-ttu-id="3fcdb-118">Les valeurs de *lParam* sont relatives à l’angle supérieur gauche d’une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="3fcdb-119">Par conséquent, pour définir l’espacement entre les icônes qui ne se chevauchent pas, les valeurs *lParam* doivent inclure la taille de l’icône, plus la quantité d’espace vide souhaitée entre les icônes.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="3fcdb-120">Les valeurs qui n’incluent pas la largeur de l’icône entraînent des chevauchements.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="3fcdb-121">Lors de la définition de l’espacement des icônes, les valeurs *lParam* doivent être définies à 4 ou plus.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="3fcdb-122">Les valeurs inférieures ne produisent pas la disposition souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="3fcdb-123">Pour réinitialiser les icônes à l’espacement par défaut, affectez la valeur-1 aux valeurs *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3fcdb-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fcdb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fcdb-124">Requirements</span></span>



| <span data-ttu-id="3fcdb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fcdb-125">Requirement</span></span> | <span data-ttu-id="3fcdb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fcdb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fcdb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fcdb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3fcdb-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fcdb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fcdb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fcdb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3fcdb-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fcdb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fcdb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fcdb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fcdb-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fcdb-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

