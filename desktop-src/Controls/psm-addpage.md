---
title: Message PSM_ADDPAGE (Prsht. h)
description: Ajoute une nouvelle page à la fin d’une feuille de propriétés existante. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844030"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="6e97e-105">Message de la \_ ADDPAGE PSM</span><span class="sxs-lookup"><span data-stu-id="6e97e-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="6e97e-106">Ajoute une nouvelle page à la fin d’une feuille de propriétés existante.</span><span class="sxs-lookup"><span data-stu-id="6e97e-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="6e97e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .</span><span class="sxs-lookup"><span data-stu-id="6e97e-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e97e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e97e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e97e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e97e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e97e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6e97e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6e97e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e97e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e97e-112">Handle vers la page à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6e97e-112">Handle to the page to add.</span></span> <span data-ttu-id="6e97e-113">La page doit avoir été créée par un appel précédent à la fonction [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="6e97e-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e97e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e97e-114">Return value</span></span>

<span data-ttu-id="6e97e-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6e97e-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e97e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6e97e-116">Remarks</span></span>

<span data-ttu-id="6e97e-117">La nouvelle page ne doit pas être supérieure à la plus grande page actuellement dans la feuille de propriétés, car la feuille de propriétés n’est pas redimensionnée pour s’ajuster à la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="6e97e-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="6e97e-118">Un certain nombre de messages et un appel de fonction se produisent pendant que la feuille de propriétés manipule la liste de pages.</span><span class="sxs-lookup"><span data-stu-id="6e97e-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="6e97e-119">Pendant cette action, toute tentative de modification de la liste de pages aura des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="6e97e-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="6e97e-120">En conséquence, vous ne devez pas utiliser le message de l' \_ PROPSHEETPAGEPROC PSM dans votre implémentation de [](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou lors de la gestion des notifications et des messages Windows suivants.</span><span class="sxs-lookup"><span data-stu-id="6e97e-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="6e97e-121">PSN \_ appliquer</span><span class="sxs-lookup"><span data-stu-id="6e97e-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="6e97e-122">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="6e97e-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="6e97e-123">\_réinitialisation PSN</span><span class="sxs-lookup"><span data-stu-id="6e97e-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="6e97e-124">PSN \_</span><span class="sxs-lookup"><span data-stu-id="6e97e-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="6e97e-125">**\_destructeur WM**</span><span class="sxs-lookup"><span data-stu-id="6e97e-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="6e97e-126">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="6e97e-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="6e97e-127">Si vous avez besoin de modifier une page de feuille de propriétés pendant que vous gérez l’un de ces messages ou lorsque [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) est en cours d’exécution, publiez un message Windows privé.</span><span class="sxs-lookup"><span data-stu-id="6e97e-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="6e97e-128">Votre application ne recevra pas ce message tant que le gestionnaire de feuille de propriétés n’aura pas terminé ses tâches.</span><span class="sxs-lookup"><span data-stu-id="6e97e-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="6e97e-129">Vous pouvez ensuite modifier la liste des pages.</span><span class="sxs-lookup"><span data-stu-id="6e97e-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e97e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e97e-130">Requirements</span></span>



| <span data-ttu-id="6e97e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e97e-131">Requirement</span></span> | <span data-ttu-id="6e97e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e97e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e97e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e97e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6e97e-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e97e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e97e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e97e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6e97e-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e97e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e97e-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e97e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e97e-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e97e-138"><dt>Prsht.h</dt></span></span> </dl> |



 

