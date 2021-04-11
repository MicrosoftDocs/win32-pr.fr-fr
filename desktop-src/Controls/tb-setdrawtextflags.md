---
title: Message TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Définit les indicateurs de dessin de texte pour la barre d’outils.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942537"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="3abf2-104">TO \_ SETDRAWTEXTFLAGS message</span><span class="sxs-lookup"><span data-stu-id="3abf2-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="3abf2-105">Définit les indicateurs de dessin de texte pour la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="3abf2-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3abf2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3abf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3abf2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3abf2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3abf2-108">Un ou plusieurs des indicateurs DT \_ , spécifiés dans [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), qui indiquent les bits de *lParam* qui seront utilisés lors du dessin du texte.</span><span class="sxs-lookup"><span data-stu-id="3abf2-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="3abf2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3abf2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3abf2-110">Un ou plusieurs des indicateurs DT \_ , spécifiés dans [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), qui indiquent comment le texte du bouton sera dessiné.</span><span class="sxs-lookup"><span data-stu-id="3abf2-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="3abf2-111">Cette valeur est transmise à la fonction **DrawText** lorsque le texte du bouton est dessiné.</span><span class="sxs-lookup"><span data-stu-id="3abf2-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3abf2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3abf2-112">Return value</span></span>

<span data-ttu-id="3abf2-113">Retourne les indicateurs de dessin de texte précédents.</span><span class="sxs-lookup"><span data-stu-id="3abf2-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="3abf2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3abf2-114">Remarks</span></span>

<span data-ttu-id="3abf2-115">Le paramètre *wParam* vous permet de spécifier les indicateurs qui seront utilisés lors du dessin du texte, même si ces indicateurs sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="3abf2-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="3abf2-116">Par exemple, si vous ne souhaitez pas que l' \_ indicateur DT Center soit utilisé lors du dessin de texte, vous devez ajouter l' \_ indicateur DT Center à *wParam* et ne pas spécifier l' \_ indicateur DT Center dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="3abf2-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="3abf2-117">Cela empêche le contrôle de passer l' \_ indicateur DT Center à la fonction [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="3abf2-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3abf2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3abf2-118">Requirements</span></span>



| <span data-ttu-id="3abf2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3abf2-119">Requirement</span></span> | <span data-ttu-id="3abf2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3abf2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3abf2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3abf2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3abf2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3abf2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3abf2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3abf2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3abf2-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3abf2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3abf2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3abf2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3abf2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3abf2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

