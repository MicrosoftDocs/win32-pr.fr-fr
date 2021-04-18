---
title: Message EM_GETSCROLLPOS (RichEdit. h)
description: Obtient la position de défilement actuelle du contrôle d’édition.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465154"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="1baac-104">\_Message GETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="1baac-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="1baac-105">Obtient la position de défilement actuelle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="1baac-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1baac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1baac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1baac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1baac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1baac-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1baac-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1baac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1baac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1baac-110">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1baac-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="1baac-111">Après avoir appelé **em \_ GETSCROLLPOS**, ce paramètre contient un point dans l’espace de texte virtuel du document, exprimé en pixels.</span><span class="sxs-lookup"><span data-stu-id="1baac-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="1baac-112">Ce point correspond au point qui se trouve actuellement dans l’angle supérieur gauche de la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="1baac-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1baac-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1baac-113">Return value</span></span>

<span data-ttu-id="1baac-114">Ce message retourne toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="1baac-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1baac-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1baac-115">Remarks</span></span>

<span data-ttu-id="1baac-116">Les valeurs retournées dans la structure [**point**](/previous-versions//dd162805(v=vs.85)) sont des valeurs 16 bits (même dans les champs de largeur 32 bits).</span><span class="sxs-lookup"><span data-stu-id="1baac-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="1baac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1baac-117">Requirements</span></span>



| <span data-ttu-id="1baac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1baac-118">Requirement</span></span> | <span data-ttu-id="1baac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1baac-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1baac-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1baac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1baac-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1baac-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1baac-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1baac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1baac-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1baac-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1baac-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1baac-124">Redistributable</span></span><br/>          | <span data-ttu-id="1baac-125">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="1baac-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1baac-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1baac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1baac-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1baac-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1baac-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1baac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baac-129">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="1baac-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

