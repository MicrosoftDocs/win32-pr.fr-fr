---
title: Message EM_GETIMEMODEBIAS (RichEdit. h)
description: Récupère le décalage de mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033056"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="36ce1-104">\_Message GETIMEMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="36ce1-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="36ce1-105">Récupère le décalage de mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36ce1-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="36ce1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36ce1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ce1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36ce1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ce1-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="36ce1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="36ce1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36ce1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ce1-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="36ce1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ce1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36ce1-111">Return value</span></span>

<span data-ttu-id="36ce1-112">Ce message retourne le paramètre de décalage en mode IME actuel.</span><span class="sxs-lookup"><span data-stu-id="36ce1-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ce1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="36ce1-113">Remarks</span></span>

<span data-ttu-id="36ce1-114">Pour récupérer le décalage en mode Text Services Framework, utilisez [**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="36ce1-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="36ce1-115">L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="36ce1-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ce1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36ce1-116">Requirements</span></span>



| <span data-ttu-id="36ce1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36ce1-117">Requirement</span></span> | <span data-ttu-id="36ce1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="36ce1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36ce1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ce1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36ce1-120">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ce1-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36ce1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ce1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36ce1-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ce1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36ce1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="36ce1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ce1-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ce1-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ce1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36ce1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="36ce1-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="36ce1-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36ce1-127">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="36ce1-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="36ce1-128">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="36ce1-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





