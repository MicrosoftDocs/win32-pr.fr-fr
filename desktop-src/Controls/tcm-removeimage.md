---
title: Message TCM_REMOVEIMAGE (commctrl. h)
description: Supprime une image de la liste d’images d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513639"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="d9035-105">\_Message REMOVEIMAGE TCM</span><span class="sxs-lookup"><span data-stu-id="d9035-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="d9035-106">Supprime une image de la liste d’images d’un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="d9035-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="d9035-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .</span><span class="sxs-lookup"><span data-stu-id="d9035-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9035-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9035-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9035-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9035-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9035-110">Index de l’image à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d9035-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="d9035-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9035-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9035-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d9035-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9035-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9035-113">Return value</span></span>

<span data-ttu-id="d9035-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d9035-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9035-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d9035-115">Remarks</span></span>

<span data-ttu-id="d9035-116">Le contrôle onglet met à jour l’index d’image de chaque onglet, de sorte que chaque onglet reste associé à la même image qu’avant.</span><span class="sxs-lookup"><span data-stu-id="d9035-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="d9035-117">Si une tabulation utilise l’image en cours de suppression, l’onglet est défini sur ne pas avoir d’image.</span><span class="sxs-lookup"><span data-stu-id="d9035-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9035-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9035-118">Requirements</span></span>



| <span data-ttu-id="d9035-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9035-119">Requirement</span></span> | <span data-ttu-id="d9035-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9035-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9035-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9035-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9035-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9035-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9035-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9035-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9035-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9035-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9035-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9035-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9035-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9035-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





