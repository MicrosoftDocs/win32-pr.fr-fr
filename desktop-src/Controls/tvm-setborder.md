---
title: Message TVM_SETBORDER (commctrl. h)
description: Définit la taille de la bordure pour les éléments dans un contrôle TreeView. Vous pouvez envoyer le message explicitement ou à l’aide de la \_ macro setBorder TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843785"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="cfded-105">TVM \_ SETBORDER message</span><span class="sxs-lookup"><span data-stu-id="cfded-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="cfded-106">**Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**</span><span class="sxs-lookup"><span data-stu-id="cfded-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="cfded-107">Définit la taille de la bordure pour les éléments dans un contrôle TreeView.</span><span class="sxs-lookup"><span data-stu-id="cfded-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="cfded-108">Vous pouvez envoyer le message explicitement ou à l’aide de la macro [**\_ setBorder TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .</span><span class="sxs-lookup"><span data-stu-id="cfded-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfded-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfded-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfded-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfded-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfded-111">Indicateurs d’action.</span><span class="sxs-lookup"><span data-stu-id="cfded-111">Action flags.</span></span> <span data-ttu-id="cfded-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfded-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="cfded-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfded-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="cfded-114">Signification</span><span class="sxs-lookup"><span data-stu-id="cfded-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="cfded-115"><dt>**TVSBF \_ XBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="cfded-116">Applique la taille de bordure spécifiée à gauche des éléments dans le contrôle TreeView.</span><span class="sxs-lookup"><span data-stu-id="cfded-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="cfded-117"><dt>**TVSBF \_ YBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="cfded-118">Applique la taille de bordure spécifiée en haut des éléments dans le contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="cfded-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="cfded-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfded-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfded-120">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **short** qui spécifie la taille de la bordure gauche, en pixels.</span><span class="sxs-lookup"><span data-stu-id="cfded-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="cfded-121">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **short** qui spécifie la taille de la bordure supérieure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="cfded-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfded-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfded-122">Return value</span></span>

<span data-ttu-id="cfded-123">Retourne une valeur de **type long** qui contient la taille de la bordure précédente, en pixels.</span><span class="sxs-lookup"><span data-stu-id="cfded-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="cfded-124">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la taille précédente de la bordure horizontale, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la taille précédente de la bordure verticale.</span><span class="sxs-lookup"><span data-stu-id="cfded-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfded-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cfded-125">Remarks</span></span>

<span data-ttu-id="cfded-126">**Avertissement de sécurité :** L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="cfded-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="cfded-127">La bordure de l’élément est définie uniquement à des fins d’espacement.</span><span class="sxs-lookup"><span data-stu-id="cfded-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="cfded-128">Un paramètre réussi déclenche un recalcul des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="cfded-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="cfded-129">Ce message n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="cfded-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="cfded-130">En outre, ce message n’est pas défini dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="cfded-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="cfded-131">Ajoutez les définitions suivantes aux fichiers sources de votre application pour utiliser le message :</span><span class="sxs-lookup"><span data-stu-id="cfded-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="cfded-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfded-132">Requirements</span></span>



| <span data-ttu-id="cfded-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfded-133">Requirement</span></span> | <span data-ttu-id="cfded-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfded-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfded-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfded-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cfded-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfded-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfded-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfded-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cfded-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfded-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfded-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfded-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfded-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfded-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfded-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfded-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfded-142">**\_SetBorder TreeView**</span><span class="sxs-lookup"><span data-stu-id="cfded-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

