---
title: Message PSM_CHANGED (Prsht. h)
description: Informe une feuille de propriétés que les informations d’une page ont été modifiées. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509126"
---
# <a name="psm_changed-message"></a><span data-ttu-id="fdd66-105">\_Message PSM modifié</span><span class="sxs-lookup"><span data-stu-id="fdd66-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="fdd66-106">Informe une feuille de propriétés que les informations d’une page ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="fdd66-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="fdd66-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .</span><span class="sxs-lookup"><span data-stu-id="fdd66-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdd66-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fdd66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdd66-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd66-110">Handle de la page qui a changé.</span><span class="sxs-lookup"><span data-stu-id="fdd66-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="fdd66-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdd66-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd66-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fdd66-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fdd66-113">Return value</span></span>

<span data-ttu-id="fdd66-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fdd66-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd66-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fdd66-115">Remarks</span></span>

<span data-ttu-id="fdd66-116">La feuille de propriétés Active le bouton **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="fdd66-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="fdd66-117">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="fdd66-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdd66-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdd66-118">Requirements</span></span>



| <span data-ttu-id="fdd66-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdd66-119">Requirement</span></span> | <span data-ttu-id="fdd66-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdd66-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd66-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdd66-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd66-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdd66-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fdd66-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdd66-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd66-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdd66-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fdd66-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdd66-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd66-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd66-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





