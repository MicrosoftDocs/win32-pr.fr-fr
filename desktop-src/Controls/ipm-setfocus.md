---
title: Message IPM_SETFOCUS (commctrl. h)
description: Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP. Tout le texte de ce champ est sélectionné.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104461"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="5eb85-105">\_Message IPM SetFocus</span><span class="sxs-lookup"><span data-stu-id="5eb85-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="5eb85-106">Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="5eb85-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="5eb85-107">Tout le texte de ce champ est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5eb85-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="5eb85-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5eb85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5eb85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb85-110">Index de champ de base zéro auquel le focus doit être défini.</span><span class="sxs-lookup"><span data-stu-id="5eb85-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="5eb85-111">Si cette valeur est supérieure au nombre de champs, le focus est défini sur le premier champ vide.</span><span class="sxs-lookup"><span data-stu-id="5eb85-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="5eb85-112">Si tous les champs ne sont pas vides, le focus est défini sur le premier champ.</span><span class="sxs-lookup"><span data-stu-id="5eb85-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="5eb85-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5eb85-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5eb85-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5eb85-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb85-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5eb85-115">Return value</span></span>

<span data-ttu-id="5eb85-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5eb85-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb85-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5eb85-117">Requirements</span></span>



| <span data-ttu-id="5eb85-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5eb85-118">Requirement</span></span> | <span data-ttu-id="5eb85-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5eb85-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb85-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eb85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb85-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5eb85-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eb85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb85-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5eb85-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5eb85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb85-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb85-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





