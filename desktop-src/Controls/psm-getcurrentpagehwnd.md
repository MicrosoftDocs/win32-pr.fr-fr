---
title: Message PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Récupère un handle de la fenêtre de la page active d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538816"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="edea2-105">\_Message PSM GETCURRENTPAGEHWND</span><span class="sxs-lookup"><span data-stu-id="edea2-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="edea2-106">Récupère un handle de la fenêtre de la page active d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="edea2-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="edea2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .</span><span class="sxs-lookup"><span data-stu-id="edea2-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="edea2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edea2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edea2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edea2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edea2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="edea2-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="edea2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edea2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edea2-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="edea2-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edea2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edea2-113">Return value</span></span>

<span data-ttu-id="edea2-114">Retourne un handle vers la fenêtre de la page de la feuille de propriétés actuelle.</span><span class="sxs-lookup"><span data-stu-id="edea2-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="edea2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="edea2-115">Remarks</span></span>

<span data-ttu-id="edea2-116">Utilisez le **message \_ GETCURRENTPAGEHWND PSM** avec les feuilles de propriétés non modales pour déterminer quand détruire la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="edea2-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="edea2-117">Quand l’utilisateur clique sur le bouton **OK** ou **Annuler** , **PSM \_ GETCURRENTPAGEHWND** retourne la **valeur null** et vous pouvez ensuite utiliser la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour détruire la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="edea2-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="edea2-118">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="edea2-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="edea2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edea2-119">Requirements</span></span>



| <span data-ttu-id="edea2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edea2-120">Requirement</span></span> | <span data-ttu-id="edea2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="edea2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edea2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edea2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edea2-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edea2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="edea2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edea2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edea2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edea2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="edea2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="edea2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="edea2-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="edea2-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edea2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edea2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edea2-129">**Feuille**</span><span class="sxs-lookup"><span data-stu-id="edea2-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

