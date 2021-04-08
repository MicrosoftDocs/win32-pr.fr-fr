---
title: Message LB_SETTABSTOPS (winuser. h)
description: Définit les positions des taquets de tabulation dans une zone de liste.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844105"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="14580-104">\_Message SETTABSTOPS lb</span><span class="sxs-lookup"><span data-stu-id="14580-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="14580-105">Définit les positions des taquets de tabulation dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="14580-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="14580-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14580-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14580-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14580-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14580-108">Spécifie le nombre de taquets de tabulation.</span><span class="sxs-lookup"><span data-stu-id="14580-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="14580-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14580-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14580-110">Pointeur vers le premier membre d’un tableau d’entiers contenant les taquets de tabulation.</span><span class="sxs-lookup"><span data-stu-id="14580-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="14580-111">Les entiers représentent le nombre de trimestres de la largeur moyenne des caractères pour la police sélectionnée dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="14580-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="14580-112">Par exemple, un taquet de tabulation de 4 est placé à 1,0 unités de caractères et un taquet de tabulation de 6 est placé à 1,5 unités de caractères moyennes.</span><span class="sxs-lookup"><span data-stu-id="14580-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="14580-113">Toutefois, si la zone de liste fait partie d’une boîte de dialogue, les entiers se trouvent dans les unités du modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="14580-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="14580-114">Les taquets de tabulation doivent être triés par ordre croissant ; les onglets en arrière ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="14580-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14580-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14580-115">Return value</span></span>

<span data-ttu-id="14580-116">Si tous les onglets spécifiés sont définis, la valeur de retour est **true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="14580-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14580-117">Notes</span><span class="sxs-lookup"><span data-stu-id="14580-117">Remarks</span></span>

<span data-ttu-id="14580-118">Pour répondre au message **lb \_ SETTABSTOPS** , la zone de liste doit avoir été créée avec le [**style \_ USETABSTOPS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="14580-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="14580-119">Si *wParam* a pour valeur 0 et *lParam* la **valeur null**, le taquet de tabulation par défaut est deux unités de modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="14580-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="14580-120">Si *wParam* est 1, la zone de liste aura des taquets de tabulation séparés par la distance spécifiée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="14580-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="14580-121">Si *lParam* pointe vers plus d’une valeur unique, un taquet de tabulation sera défini pour chaque valeur dans *lParam*, jusqu’au nombre spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="14580-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="14580-122">Les valeurs spécifiées par *lParam* se trouvent dans les unités de modèle de boîte de dialogue, qui sont les unités indépendantes du périphérique utilisées dans les modèles de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="14580-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="14580-123">Pour convertir des mesures à partir d’unités de modèle de boîte de dialogue en unités d’écran (pixels), utilisez la fonction [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="14580-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="14580-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : la mémoire tampon désignée par *lParam* doit résider dans la mémoire accessible en écriture, même si le message ne modifie pas le tableau.</span><span class="sxs-lookup"><span data-stu-id="14580-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="14580-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14580-125">Requirements</span></span>



| <span data-ttu-id="14580-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14580-126">Requirement</span></span> | <span data-ttu-id="14580-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="14580-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14580-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14580-128">Minimum supported client</span></span><br/> | <span data-ttu-id="14580-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14580-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14580-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14580-130">Minimum supported server</span></span><br/> | <span data-ttu-id="14580-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14580-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14580-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="14580-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="14580-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14580-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14580-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14580-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14580-135">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="14580-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

