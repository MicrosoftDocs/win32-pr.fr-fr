---
title: Message CB_GETMINVISIBLE (commctrl. h)
description: Obtient le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843566"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="a67d1-104">\_Message GETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="a67d1-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="a67d1-105">Obtient le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a67d1-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a67d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a67d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a67d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a67d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a67d1-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a67d1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a67d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a67d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a67d1-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a67d1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a67d1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a67d1-111">Return value</span></span>

<span data-ttu-id="a67d1-112">La valeur de retour est le nombre minimal d’éléments visibles.</span><span class="sxs-lookup"><span data-stu-id="a67d1-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="a67d1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a67d1-113">Remarks</span></span>

<span data-ttu-id="a67d1-114">Lorsque le nombre d’éléments dans la liste déroulante est supérieur au minimum, la zone de liste déroulante utilise une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="a67d1-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="a67d1-115">Ce message est ignoré si le contrôle de zone de liste déroulante a un [**\_ NOINTEGRALHEIGHT SCC**](combo-box-styles.md)de style.</span><span class="sxs-lookup"><span data-stu-id="a67d1-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="a67d1-116">Pour utiliser **CB \_ GETMINVISIBLE**, l’application doit spécifier comctl32.dll version 6 dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="a67d1-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="a67d1-117">Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a67d1-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a67d1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a67d1-118">Requirements</span></span>



| <span data-ttu-id="a67d1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a67d1-119">Requirement</span></span> | <span data-ttu-id="a67d1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67d1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a67d1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a67d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a67d1-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a67d1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a67d1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a67d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a67d1-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a67d1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a67d1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a67d1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a67d1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a67d1-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67d1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a67d1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a67d1-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a67d1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a67d1-129">**\_SETMINVISIBLE CB**</span><span class="sxs-lookup"><span data-stu-id="a67d1-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="a67d1-130">**\_GetMinVisible ComboBox**</span><span class="sxs-lookup"><span data-stu-id="a67d1-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





