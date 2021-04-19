---
title: Message PSM_INSERTPAGE (Prsht. h)
description: Insère une nouvelle page dans une feuille de propriétés existante. La page peut être insérée à un index spécifié ou après une page spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538812"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="1e4b9-106">\_Message PSM INSERTPAGE</span><span class="sxs-lookup"><span data-stu-id="1e4b9-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="1e4b9-107">Insère une nouvelle page dans une feuille de propriétés existante.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="1e4b9-108">La page peut être insérée à un index spécifié ou après une page spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="1e4b9-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .</span><span class="sxs-lookup"><span data-stu-id="1e4b9-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e4b9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e4b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4b9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e4b9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4b9-112">Où la page doit être insérée.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-112">Where the page is to be inserted.</span></span> <span data-ttu-id="1e4b9-113">Affectez la valeur **null** à ce paramètre pour faire de la nouvelle page la première page.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="1e4b9-114">Pour spécifier l’emplacement où la nouvelle page doit être insérée, vous pouvez passer un index ou le handle HPROPSHEETPAGE d’une page existante.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="1e4b9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e4b9-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="1e4b9-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1e4b9-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e4b9-117"><dt></dt><dt>index</dt></span><span class="sxs-lookup"><span data-stu-id="1e4b9-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="1e4b9-118">Si le paramètre *wParam* est inférieur à MAXUSHORT (l’entier Short non signé le plus grand), *wParam* spécifie l’index de base zéro de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="1e4b9-119">Par exemple, pour faire de la page insérée la troisième page sur la feuille de propriétés, affectez la valeur 2 à *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1e4b9-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="1e4b9-120">Pour en faire la première page, affectez la valeur 0 à *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1e4b9-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="1e4b9-121">Si *wParam* a une valeur supérieure au nombre de pages et inférieure à MAXUSHORT, la page est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="1e4b9-122"><dt></dt><dt>hpageInsertAfter</dt></span><span class="sxs-lookup"><span data-stu-id="1e4b9-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="1e4b9-123">Si vous définissez le paramètre *wParam* sur le handle HPROPSHEETPAGE d’une page existante, la nouvelle page est insérée après celle-ci.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="1e4b9-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e4b9-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4b9-125">Handle vers la page à insérer.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="1e4b9-126">La page doit d’abord être créée par un appel à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="1e4b9-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e4b9-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e4b9-127">Return value</span></span>

<span data-ttu-id="1e4b9-128">Retourne une valeur différente de zéro si la page a été correctement insérée, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e4b9-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1e4b9-129">Remarks</span></span>

<span data-ttu-id="1e4b9-130">Les pages après le point d’insertion sont décalées vers la droite pour s’adapter à la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="1e4b9-131">La feuille de propriétés n’est pas redimensionnée pour s’ajuster à la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="1e4b9-132">Ne rendez pas la nouvelle page plus grande que la page la plus grande de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="1e4b9-133">Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="1e4b9-134">Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="1e4b9-135">En conséquence, vous ne devez pas utiliser le \_ message PSM INSERTPAGE dans votre implémentation de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou pendant la gestion des notifications et des messages Windows suivants.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="1e4b9-136">PSN \_ appliquer</span><span class="sxs-lookup"><span data-stu-id="1e4b9-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="1e4b9-137">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="1e4b9-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="1e4b9-138">\_réinitialisation PSN</span><span class="sxs-lookup"><span data-stu-id="1e4b9-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="1e4b9-139">PSN \_</span><span class="sxs-lookup"><span data-stu-id="1e4b9-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="1e4b9-140">**\_destructeur WM**</span><span class="sxs-lookup"><span data-stu-id="1e4b9-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="1e4b9-141">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="1e4b9-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="1e4b9-142">Si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="1e4b9-143">Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="1e4b9-144">Vous pouvez ensuite modifier la liste des pages.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="1e4b9-145">Les notifications suivantes sont également affectées par la modification de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="1e4b9-146">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="1e4b9-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="1e4b9-147">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="1e4b9-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="1e4b9-148">Vous pouvez ajouter ou supprimer des pages en réponse à ces notifications, à condition que vous reveniez (via DWL \_ MSGRESULT) une valeur différente de zéro pour spécifier la nouvelle page souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="1e4b9-149">Notez, toutefois, que si vous insérez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.</span><span class="sxs-lookup"><span data-stu-id="1e4b9-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="1e4b9-150">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="1e4b9-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e4b9-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e4b9-151">Requirements</span></span>



| <span data-ttu-id="1e4b9-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e4b9-152">Requirement</span></span> | <span data-ttu-id="1e4b9-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e4b9-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4b9-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e4b9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4b9-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e4b9-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1e4b9-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e4b9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4b9-157">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e4b9-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1e4b9-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e4b9-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e4b9-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4b9-159"><dt>Prsht.h</dt></span></span> </dl> |



 

