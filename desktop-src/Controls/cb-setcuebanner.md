---
title: Message CB_SETCUEBANNER (winuser. h)
description: Définit le texte de bannière de signal qui est affiché pour le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032846"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="12d82-104">\_Message SETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="12d82-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="12d82-105">Définit le texte de bannière de signal qui est affiché pour le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="12d82-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="12d82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12d82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12d82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12d82-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="12d82-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="12d82-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12d82-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12d82-110">Pointeur vers une mémoire tampon de chaîne Unicode se terminant par un caractère null qui contient le texte.</span><span class="sxs-lookup"><span data-stu-id="12d82-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d82-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12d82-111">Return value</span></span>

<span data-ttu-id="12d82-112">Retourne 1 en cas de réussite, ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="12d82-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d82-113">Notes</span><span class="sxs-lookup"><span data-stu-id="12d82-113">Remarks</span></span>

<span data-ttu-id="12d82-114">La bannière de signal est du texte affiché dans le contrôle d’édition d’une zone de liste déroulante lorsqu’il n’y a aucune sélection.</span><span class="sxs-lookup"><span data-stu-id="12d82-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d82-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12d82-115">Requirements</span></span>



| <span data-ttu-id="12d82-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12d82-116">Requirement</span></span> | <span data-ttu-id="12d82-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="12d82-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d82-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12d82-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12d82-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12d82-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12d82-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12d82-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12d82-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="12d82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d82-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d82-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d82-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12d82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d82-125">Fonctionnalités de zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="12d82-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





