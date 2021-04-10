---
title: Message PSM_UNCHANGED (Prsht. h)
description: Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet inchangée.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200578"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="614b6-105">Message PSM non \_ modifié</span><span class="sxs-lookup"><span data-stu-id="614b6-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="614b6-106">Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment.</span><span class="sxs-lookup"><span data-stu-id="614b6-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="614b6-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ inchangée**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .</span><span class="sxs-lookup"><span data-stu-id="614b6-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="614b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="614b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614b6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="614b6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="614b6-110">Handle vers la page qui a rétabli l’état enregistré précédemment.</span><span class="sxs-lookup"><span data-stu-id="614b6-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="614b6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="614b6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="614b6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="614b6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="614b6-113">Return value</span></span>

<span data-ttu-id="614b6-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="614b6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="614b6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="614b6-115">Remarks</span></span>

<span data-ttu-id="614b6-116">La feuille des propriétés désactive le bouton **appliquer** si aucune autre page n’a enregistré des modifications dans la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="614b6-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="614b6-117">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="614b6-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="614b6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="614b6-118">Requirements</span></span>



| <span data-ttu-id="614b6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="614b6-119">Requirement</span></span> | <span data-ttu-id="614b6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="614b6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="614b6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="614b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="614b6-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="614b6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="614b6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="614b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="614b6-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="614b6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="614b6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="614b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="614b6-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="614b6-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





