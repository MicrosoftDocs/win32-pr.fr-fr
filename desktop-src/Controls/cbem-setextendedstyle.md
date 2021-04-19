---
title: Message CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Définit des styles étendus dans un contrôle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513640"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="4e6a2-104">\_Message CBEM SETEXTENDEDSTYLE</span><span class="sxs-lookup"><span data-stu-id="4e6a2-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="4e6a2-105">Définit des styles étendus dans un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e6a2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e6a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e6a2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e6a2-108">Valeur **DWORD** qui indique les styles de *lParam* à affecter.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="4e6a2-109">Seuls les styles étendus dans *wParam* seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="4e6a2-110">Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="4e6a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e6a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e6a2-112">Valeur **DWORD** qui contient les [styles étendus de contrôle ComboBoxEx](comboboxex-control-extended-styles.md) à définir pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6a2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e6a2-113">Return value</span></span>

<span data-ttu-id="4e6a2-114">Retourne une valeur **DWORD** qui contient les styles étendus utilisés précédemment pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e6a2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4e6a2-115">Remarks</span></span>

<span data-ttu-id="4e6a2-116">*wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="4e6a2-117">Par exemple, si vous transmettez [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) pour *wParam* et 0 pour *lParam*, le style **CBES \_ ex \_ NOEDITIMAGE** sera effacé, mais tous les autres styles resteront les mêmes.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="4e6a2-118">Si vous essayez de définir un style étendu pour un contrôle ComboBoxEx créé avec le style [**CBS \_ simple**](combo-box-styles.md) , il se peut qu’il ne redessine pas correctement.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6a2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e6a2-119">Requirements</span></span>



| <span data-ttu-id="4e6a2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e6a2-120">Requirement</span></span> | <span data-ttu-id="4e6a2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e6a2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6a2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e6a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4e6a2-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e6a2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e6a2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e6a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4e6a2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e6a2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e6a2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e6a2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e6a2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e6a2-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





