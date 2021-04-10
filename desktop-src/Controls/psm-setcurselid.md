---
title: Message PSM_SETCURSELID (Prsht. h)
description: Active la page donnée dans une feuille de propriétés en fonction de l’identificateur de ressource de la page. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105085"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="b654b-105">\_Message PSM SETCURSELID</span><span class="sxs-lookup"><span data-stu-id="b654b-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="b654b-106">Active la page donnée dans une feuille de propriétés en fonction de l’identificateur de ressource de la page.</span><span class="sxs-lookup"><span data-stu-id="b654b-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="b654b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .</span><span class="sxs-lookup"><span data-stu-id="b654b-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b654b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b654b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b654b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b654b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b654b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b654b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b654b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b654b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b654b-112">Identificateur de ressource de la page à activer.</span><span class="sxs-lookup"><span data-stu-id="b654b-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b654b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b654b-113">Return value</span></span>

<span data-ttu-id="b654b-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b654b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b654b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b654b-115">Remarks</span></span>

<span data-ttu-id="b654b-116">La fenêtre qui perd l’activation reçoit le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) , et la fenêtre qui obtient l’activation reçoit le code de [notification \_ PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="b654b-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b654b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b654b-117">Requirements</span></span>



| <span data-ttu-id="b654b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b654b-118">Requirement</span></span> | <span data-ttu-id="b654b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b654b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b654b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b654b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b654b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b654b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b654b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b654b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b654b-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b654b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b654b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b654b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b654b-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b654b-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





