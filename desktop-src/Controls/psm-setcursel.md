---
title: Message PSM_SETCURSEL (Prsht. h)
description: Active la page spécifiée dans une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetCurSel.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103469"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="de9ac-105">\_Message PSM SETCURSEL</span><span class="sxs-lookup"><span data-stu-id="de9ac-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="de9ac-106">Active la page spécifiée dans une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="de9ac-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="de9ac-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="de9ac-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="de9ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de9ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9ac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de9ac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de9ac-110">Index de base zéro de la page.</span><span class="sxs-lookup"><span data-stu-id="de9ac-110">The zero-based index of the page.</span></span> <span data-ttu-id="de9ac-111">Une application peut spécifier l’index ou le descripteur, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="de9ac-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="de9ac-112">Si les deux sont spécifiés, *lParam* est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="de9ac-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="de9ac-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de9ac-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de9ac-114">Handle vers la page à activer.</span><span class="sxs-lookup"><span data-stu-id="de9ac-114">The handle to the page to activate.</span></span> <span data-ttu-id="de9ac-115">Une application peut spécifier l’index ou le descripteur, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="de9ac-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="de9ac-116">Si les deux sont spécifiés, *lParam* est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="de9ac-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9ac-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de9ac-117">Return value</span></span>

<span data-ttu-id="de9ac-118">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="de9ac-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9ac-119">Notes</span><span class="sxs-lookup"><span data-stu-id="de9ac-119">Remarks</span></span>

<span data-ttu-id="de9ac-120">La fenêtre qui perd l’activation reçoit le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) , et la fenêtre qui obtient l’activation reçoit le code de [notification \_ PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="de9ac-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9ac-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de9ac-121">Requirements</span></span>



| <span data-ttu-id="de9ac-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de9ac-122">Requirement</span></span> | <span data-ttu-id="de9ac-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="de9ac-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de9ac-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de9ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="de9ac-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de9ac-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de9ac-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de9ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="de9ac-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de9ac-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="de9ac-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="de9ac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="de9ac-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9ac-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





