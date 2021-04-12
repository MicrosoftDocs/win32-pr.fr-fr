---
title: Message CB_SHOWDROPDOWN (winuser. h)
description: Une application envoie un \_ message CB SHOWDROPDOWN pour afficher ou masquer la zone de liste d’une zone de liste déroulante avec le \_ style déroulant CBS ou le \_ style DropDownList SCC.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105604"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="eb113-104">\_Message SHOWDROPDOWN CB</span><span class="sxs-lookup"><span data-stu-id="eb113-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="eb113-105">Une application envoie un message **CB \_ SHOWDROPDOWN** pour afficher ou masquer la zone de liste d’une zone de liste déroulante avec le style [**\_ déroulant CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="eb113-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb113-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb113-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb113-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb113-108">Valeur **booléenne** qui spécifie si la zone de liste déroulante doit être affichée ou masquée.</span><span class="sxs-lookup"><span data-stu-id="eb113-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="eb113-109">La valeur **true** affiche la zone de liste ; la valeur **false** le masque.</span><span class="sxs-lookup"><span data-stu-id="eb113-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="eb113-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb113-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb113-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="eb113-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb113-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb113-112">Return value</span></span>

<span data-ttu-id="eb113-113">La valeur de retour est toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="eb113-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb113-114">Notes</span><span class="sxs-lookup"><span data-stu-id="eb113-114">Remarks</span></span>

<span data-ttu-id="eb113-115">Ce message n’a aucun effet sur une zone de liste déroulante créée avec le style [**\_ simple CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="eb113-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb113-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb113-116">Requirements</span></span>



| <span data-ttu-id="eb113-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb113-117">Requirement</span></span> | <span data-ttu-id="eb113-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb113-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb113-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb113-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb113-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb113-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb113-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb113-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb113-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb113-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb113-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb113-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb113-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb113-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb113-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb113-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb113-126">**\_GETDROPPEDSTATE CB**</span><span class="sxs-lookup"><span data-stu-id="eb113-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





