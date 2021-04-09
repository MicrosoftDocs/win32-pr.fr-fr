---
title: Message PSM_SETTITLE (Prsht. h)
description: Définit le titre d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941707"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="9dca0-105">\_Message PSM SETTITLE</span><span class="sxs-lookup"><span data-stu-id="9dca0-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="9dca0-106">Définit le titre d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9dca0-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="9dca0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .</span><span class="sxs-lookup"><span data-stu-id="9dca0-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9dca0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9dca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dca0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9dca0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dca0-110">Indicateur qui spécifie s’il faut inclure le préfixe « Properties for » ou le suffixe « Properties » (selon la version) avec la chaîne de titre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9dca0-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="9dca0-111">Si cette valeur est PSH \_ PROPTITLE, le préfixe ou le suffixe est inclus.</span><span class="sxs-lookup"><span data-stu-id="9dca0-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="9dca0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dca0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dca0-113">Pointeur vers une mémoire tampon qui contient la chaîne de titre.</span><span class="sxs-lookup"><span data-stu-id="9dca0-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="9dca0-114">Si le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de ce paramètre a la **valeur null**, la feuille de propriétés charge la ressource de type chaîne spécifiée dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9dca0-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dca0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9dca0-115">Return value</span></span>

<span data-ttu-id="9dca0-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9dca0-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dca0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9dca0-117">Remarks</span></span>

<span data-ttu-id="9dca0-118">Dans un Assistant Aero, ce message peut être utilisé pour modifier le titre d’une page intérieure de manière dynamique ; par exemple, lors de la gestion de la notification [ \_ SetActive PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="9dca0-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dca0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dca0-119">Requirements</span></span>



| <span data-ttu-id="9dca0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dca0-120">Requirement</span></span> | <span data-ttu-id="9dca0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dca0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9dca0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dca0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9dca0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dca0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9dca0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dca0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9dca0-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dca0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9dca0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dca0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dca0-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dca0-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="9dca0-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9dca0-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9dca0-129">**PSM \_ SETTITLEW** (Unicode) et **PSM \_ SETTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9dca0-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

