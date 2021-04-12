---
title: Message EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Retourne l’état actuel des options typographiques d’un contrôle RichEdit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105106"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="1e45e-104">\_Message GETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="1e45e-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="1e45e-105">Retourne l’état actuel des options typographiques d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="1e45e-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e45e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e45e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e45e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e45e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e45e-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1e45e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e45e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e45e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e45e-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1e45e-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e45e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e45e-111">Return value</span></span>

<span data-ttu-id="1e45e-112">Retourne les options typographiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="1e45e-112">Returns the current typography options.</span></span> <span data-ttu-id="1e45e-113">Pour obtenir la liste des options, consultez [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="1e45e-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e45e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1e45e-114">Remarks</span></span>

<span data-ttu-id="1e45e-115">Vous pouvez activer le saut de ligne avancé en envoyant le message [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="1e45e-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="1e45e-116">Le saut de ligne avancé et normal peut également être activé automatiquement par le contrôle Rich Edit s’il est nécessaire pour certaines langues.</span><span class="sxs-lookup"><span data-stu-id="1e45e-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e45e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e45e-117">Requirements</span></span>



| <span data-ttu-id="1e45e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e45e-118">Requirement</span></span> | <span data-ttu-id="1e45e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e45e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e45e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e45e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1e45e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e45e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e45e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e45e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1e45e-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e45e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e45e-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1e45e-124">Redistributable</span></span><br/>          | <span data-ttu-id="1e45e-125">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="1e45e-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1e45e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e45e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e45e-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e45e-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e45e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e45e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e45e-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1e45e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e45e-130">**\_SETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="1e45e-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="1e45e-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1e45e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e45e-132">À propos des contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="1e45e-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





