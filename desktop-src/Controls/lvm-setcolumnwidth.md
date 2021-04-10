---
title: Message LVM_SETCOLUMNWIDTH (commctrl. h)
description: Modifie la largeur d’une colonne en mode rapport ou la largeur de toutes les colonnes en mode affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetColumnWidth.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102892"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="30c0a-105">\_Message SETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="30c0a-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="30c0a-106">Modifie la largeur d’une colonne en mode rapport ou la largeur de toutes les colonnes en mode affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="30c0a-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="30c0a-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="30c0a-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30c0a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30c0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30c0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30c0a-110">Index de base zéro d’une colonne valide.</span><span class="sxs-lookup"><span data-stu-id="30c0a-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="30c0a-111">Pour le mode affichage de liste, ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="30c0a-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="30c0a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30c0a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30c0a-113">Nouvelle largeur de la colonne, en pixels.</span><span class="sxs-lookup"><span data-stu-id="30c0a-113">New width of the column, in pixels.</span></span> <span data-ttu-id="30c0a-114">Pour le mode rapport-vue, les valeurs spéciales suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="30c0a-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="30c0a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c0a-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="30c0a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="30c0a-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="30c0a-117"><dt>**\_REdimensionnement automatique LVSCW**</dt></span><span class="sxs-lookup"><span data-stu-id="30c0a-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="30c0a-118">Dimensionne automatiquement la colonne.</span><span class="sxs-lookup"><span data-stu-id="30c0a-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="30c0a-119"><dt>**LVSCW \_ AutoSize \_ USEHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="30c0a-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="30c0a-120">Dimensionne automatiquement la colonne pour qu’elle corresponde au texte d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="30c0a-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="30c0a-121">Si vous utilisez cette valeur avec la dernière colonne, sa largeur est définie pour remplir la largeur restante du contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="30c0a-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c0a-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30c0a-122">Return value</span></span>

<span data-ttu-id="30c0a-123">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="30c0a-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30c0a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="30c0a-124">Remarks</span></span>

<span data-ttu-id="30c0a-125">Supposons que vous disposez d’un contrôle de vue de liste de 2 colonnes avec une largeur de 500 pixels.</span><span class="sxs-lookup"><span data-stu-id="30c0a-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="30c0a-126">Si la largeur de la colonne zéro est définie sur 200 pixels, et que vous envoyez ce message avec *wParam* = 1 et *lParam* = LVSCW \_ AutoSize \_ USEHEADER, la deuxième colonne (et la dernière) aura une largeur de 300 pixels.</span><span class="sxs-lookup"><span data-stu-id="30c0a-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c0a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30c0a-127">Requirements</span></span>



| <span data-ttu-id="30c0a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30c0a-128">Requirement</span></span> | <span data-ttu-id="30c0a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c0a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30c0a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c0a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30c0a-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c0a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30c0a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c0a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30c0a-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c0a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30c0a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="30c0a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c0a-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c0a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





