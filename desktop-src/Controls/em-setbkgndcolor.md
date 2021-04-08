---
title: Message EM_SETBKGNDCOLOR (RichEdit. h)
description: Le \_ message SETBKGNDCOLOR em définit la couleur d’arrière-plan d’un contrôle RichEdit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844133"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="2d504-104">\_Message SETBKGNDCOLOR em</span><span class="sxs-lookup"><span data-stu-id="2d504-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="2d504-105">Le **message \_ SETBKGNDCOLOR em** définit la couleur d’arrière-plan d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="2d504-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d504-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d504-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d504-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d504-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d504-108">Spécifie s’il faut utiliser la couleur système.</span><span class="sxs-lookup"><span data-stu-id="2d504-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="2d504-109">Si ce paramètre est une valeur différente de zéro, l’arrière-plan est défini sur la couleur système d’arrière-plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2d504-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="2d504-110">Dans le cas contraire, l’arrière-plan est défini sur la couleur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d504-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="2d504-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d504-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d504-112">Structure [**COLORREF**](/windows/desktop/gdi/colorref) spécifiant la couleur si *wParam* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2d504-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="2d504-113">Pour générer **COLORREF**, utilisez la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="2d504-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d504-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d504-114">Return value</span></span>

<span data-ttu-id="2d504-115">Ce message retourne la couleur d’arrière-plan d’origine.</span><span class="sxs-lookup"><span data-stu-id="2d504-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d504-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d504-116">Requirements</span></span>



| <span data-ttu-id="2d504-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d504-117">Requirement</span></span> | <span data-ttu-id="2d504-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d504-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d504-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d504-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d504-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d504-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d504-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d504-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d504-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d504-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d504-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d504-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d504-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d504-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d504-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d504-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d504-126">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="2d504-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2d504-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="2d504-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="2d504-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2d504-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

