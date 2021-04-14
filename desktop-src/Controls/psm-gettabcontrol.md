---
title: Message PSM_GETTABCONTROL (Prsht. h)
description: Récupère le handle du contrôle onglet d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509074"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="063cc-105">\_Message PSM GETTABCONTROL</span><span class="sxs-lookup"><span data-stu-id="063cc-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="063cc-106">Récupère le handle du contrôle onglet d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="063cc-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="063cc-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .</span><span class="sxs-lookup"><span data-stu-id="063cc-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="063cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="063cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="063cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="063cc-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="063cc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="063cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="063cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="063cc-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="063cc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063cc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="063cc-113">Return value</span></span>

<span data-ttu-id="063cc-114">Retourne le handle du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="063cc-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="063cc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="063cc-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="063cc-116">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="063cc-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="063cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="063cc-117">Requirements</span></span>



| <span data-ttu-id="063cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="063cc-118">Requirement</span></span> | <span data-ttu-id="063cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="063cc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="063cc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="063cc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="063cc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="063cc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="063cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="063cc-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="063cc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="063cc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="063cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="063cc-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="063cc-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





