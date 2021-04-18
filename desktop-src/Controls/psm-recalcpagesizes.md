---
title: Message PSM_RECALCPAGESIZES (Prsht. h)
description: Recalcule la taille de page d’une feuille de propriétés standard ou d’Assistant après l’ajout ou la suppression de pages. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509547"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="cbb24-105">\_Message PSM RECALCPAGESIZES</span><span class="sxs-lookup"><span data-stu-id="cbb24-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="cbb24-106">Recalcule la taille de page d’une feuille de propriétés standard ou d’Assistant après l’ajout ou la suppression de pages.</span><span class="sxs-lookup"><span data-stu-id="cbb24-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="cbb24-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .</span><span class="sxs-lookup"><span data-stu-id="cbb24-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbb24-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbb24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbb24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb24-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cbb24-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cbb24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbb24-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb24-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cbb24-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb24-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbb24-113">Return value</span></span>

<span data-ttu-id="cbb24-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cbb24-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb24-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cbb24-115">Remarks</span></span>

<span data-ttu-id="cbb24-116">Lorsqu’une feuille de propriétés est créée, elle est dimensionnée pour correspondre à sa collection initiale de pages.</span><span class="sxs-lookup"><span data-stu-id="cbb24-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="cbb24-117">Pour assurer la compatibilité avec les versions précédentes des contrôles communs, les feuilles de propriétés et les assistants ne se redimensionnent pas automatiquement quand les pages sont ajoutées ou supprimées par la suite.</span><span class="sxs-lookup"><span data-stu-id="cbb24-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="cbb24-118">Avec les contrôles communs [version 5,80](common-control-versions.md), les applications doivent envoyer un message **PSM \_ RECALCPAGESIZES** après l’ajout ou la suppression de pages avec [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)ou leurs macros équivalentes.</span><span class="sxs-lookup"><span data-stu-id="cbb24-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="cbb24-119">Elle garantit que la feuille de propriétés est correctement dimensionnée pour sa collection de pages actuelle.</span><span class="sxs-lookup"><span data-stu-id="cbb24-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="cbb24-120">Si ce message n’est pas envoyé, certaines pages de la feuille de propriétés peuvent être tronquées ou trop volumineuses.</span><span class="sxs-lookup"><span data-stu-id="cbb24-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="cbb24-121">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="cbb24-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbb24-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbb24-122">Requirements</span></span>



| <span data-ttu-id="cbb24-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbb24-123">Requirement</span></span> | <span data-ttu-id="cbb24-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbb24-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb24-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbb24-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb24-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbb24-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cbb24-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbb24-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb24-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbb24-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cbb24-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbb24-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbb24-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbb24-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 





