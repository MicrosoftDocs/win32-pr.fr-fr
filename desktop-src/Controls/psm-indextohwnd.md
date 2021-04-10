---
title: Message PSM_INDEXTOHWND (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son handle de fenêtre. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToHwnd.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- PSM_INDEXTOHWND les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105262"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="2f97d-105">\_Message PSM INDEXTOHWND</span><span class="sxs-lookup"><span data-stu-id="2f97d-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="2f97d-106">Prend l’index d’une page de feuille de propriétés et retourne son handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2f97d-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="2f97d-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .</span><span class="sxs-lookup"><span data-stu-id="2f97d-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f97d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f97d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f97d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f97d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f97d-110">Index de base zéro de la page.</span><span class="sxs-lookup"><span data-stu-id="2f97d-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="2f97d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f97d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f97d-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f97d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f97d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f97d-113">Return value</span></span>

<span data-ttu-id="2f97d-114">Retourne le handle de la fenêtre de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2f97d-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="2f97d-115">Sinon, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2f97d-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f97d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f97d-116">Requirements</span></span>



| <span data-ttu-id="2f97d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f97d-117">Requirement</span></span> | <span data-ttu-id="2f97d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f97d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f97d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f97d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2f97d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f97d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f97d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f97d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2f97d-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f97d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f97d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f97d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f97d-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f97d-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





