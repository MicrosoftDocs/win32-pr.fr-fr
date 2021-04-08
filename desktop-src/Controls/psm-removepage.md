---
title: Message PSM_REMOVEPAGE (Prsht. h)
description: Supprime une page d'une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844025"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="ddf21-105">\_Message PSM REMOVEPAGE</span><span class="sxs-lookup"><span data-stu-id="ddf21-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="ddf21-106">Supprime une page d'une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddf21-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="ddf21-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .</span><span class="sxs-lookup"><span data-stu-id="ddf21-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddf21-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddf21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddf21-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf21-110">Index de base zéro de la page à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ddf21-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="ddf21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddf21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf21-112">Handle HPROPSHEETPAGE de la page à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ddf21-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf21-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddf21-113">Return value</span></span>

<span data-ttu-id="ddf21-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ddf21-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddf21-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ddf21-115">Remarks</span></span>

<span data-ttu-id="ddf21-116">Une application peut spécifier l’index ou le descripteur, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="ddf21-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="ddf21-117">Si les deux sont spécifiés, *lParam* est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="ddf21-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="ddf21-118">L’envoi de **\_ REMOVEPAGE PSM** détruit la page de la feuille de propriétés qui est supprimée.</span><span class="sxs-lookup"><span data-stu-id="ddf21-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="ddf21-119">Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages.</span><span class="sxs-lookup"><span data-stu-id="ddf21-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="ddf21-120">Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="ddf21-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="ddf21-121">En conséquence, vous ne devez pas utiliser le message **PSM \_ REMOVEPAGE** dans votre implémentation de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou pendant la gestion des notifications et des messages Windows suivants.</span><span class="sxs-lookup"><span data-stu-id="ddf21-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="ddf21-122">PSN \_ appliquer</span><span class="sxs-lookup"><span data-stu-id="ddf21-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="ddf21-123">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="ddf21-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="ddf21-124">\_réinitialisation PSN</span><span class="sxs-lookup"><span data-stu-id="ddf21-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="ddf21-125">PSN \_</span><span class="sxs-lookup"><span data-stu-id="ddf21-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="ddf21-126">**\_destructeur WM**</span><span class="sxs-lookup"><span data-stu-id="ddf21-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="ddf21-127">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="ddf21-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="ddf21-128">Si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé.</span><span class="sxs-lookup"><span data-stu-id="ddf21-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="ddf21-129">Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches.</span><span class="sxs-lookup"><span data-stu-id="ddf21-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="ddf21-130">Vous pouvez ensuite modifier la liste des pages.</span><span class="sxs-lookup"><span data-stu-id="ddf21-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="ddf21-131">Les notifications suivantes sont également affectées par la modification de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddf21-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="ddf21-132">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="ddf21-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="ddf21-133">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="ddf21-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="ddf21-134">Vous pouvez ajouter ou supprimer des pages en réponse à ces notifications, à condition que vous reveniez (via DWL \_ MSGRESULT) une valeur différente de zéro pour spécifier la nouvelle page souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ddf21-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="ddf21-135">Notez, toutefois, que si vous supprimez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.</span><span class="sxs-lookup"><span data-stu-id="ddf21-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf21-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddf21-136">Requirements</span></span>



| <span data-ttu-id="ddf21-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddf21-137">Requirement</span></span> | <span data-ttu-id="ddf21-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddf21-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf21-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddf21-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf21-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddf21-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ddf21-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddf21-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf21-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddf21-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ddf21-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddf21-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf21-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf21-144"><dt>Prsht.h</dt></span></span> </dl> |



 

