---
title: Message CB_SETMINVISIBLE (commctrl. h)
description: Une application envoie un \_ message CB SETMINVISIBLE pour définir le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102985"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="a24f1-104">\_Message SETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="a24f1-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="a24f1-105">Une application envoie un message **CB \_ SETMINVISIBLE** pour définir le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a24f1-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a24f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a24f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a24f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24f1-108">Spécifie le nombre minimal d’éléments visibles.</span><span class="sxs-lookup"><span data-stu-id="a24f1-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="a24f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a24f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24f1-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="a24f1-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24f1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a24f1-111">Return value</span></span>

<span data-ttu-id="a24f1-112">Si le message réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="a24f1-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="a24f1-113">Sinon, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="a24f1-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24f1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a24f1-114">Remarks</span></span>

<span data-ttu-id="a24f1-115">Lorsque le nombre d’éléments dans la liste déroulante est supérieur au minimum, la zone de liste déroulante utilise une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="a24f1-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="a24f1-116">Par défaut, 30 est le nombre minimal d’éléments visibles.</span><span class="sxs-lookup"><span data-stu-id="a24f1-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="a24f1-117">Ce message est ignoré si le contrôle de zone de liste déroulante a un [**\_ NOINTEGRALHEIGHT SCC**](combo-box-styles.md)de style.</span><span class="sxs-lookup"><span data-stu-id="a24f1-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="a24f1-118">Pour utiliser **CB \_ SETMINVISIBLE**, l’application doit spécifier comctl32.dll version 6 dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="a24f1-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="a24f1-119">Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a24f1-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a24f1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a24f1-120">Requirements</span></span>



| <span data-ttu-id="a24f1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a24f1-121">Requirement</span></span> | <span data-ttu-id="a24f1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a24f1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a24f1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a24f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a24f1-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a24f1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a24f1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a24f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a24f1-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a24f1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a24f1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a24f1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24f1-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a24f1-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24f1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a24f1-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a24f1-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a24f1-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a24f1-131">**\_GETMINVISIBLE CB**</span><span class="sxs-lookup"><span data-stu-id="a24f1-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="a24f1-132">**\_SetMinVisible ComboBox**</span><span class="sxs-lookup"><span data-stu-id="a24f1-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





