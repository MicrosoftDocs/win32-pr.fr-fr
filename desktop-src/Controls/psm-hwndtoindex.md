---
title: Message PSM_HWNDTOINDEX (Prsht. h)
description: Prend le handle de fenêtre de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104197"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="9b92e-105">\_Message PSM HWNDTOINDEX</span><span class="sxs-lookup"><span data-stu-id="9b92e-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="9b92e-106">Prend le handle de fenêtre de la page de la feuille de propriétés et retourne son index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="9b92e-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="9b92e-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .</span><span class="sxs-lookup"><span data-stu-id="9b92e-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b92e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b92e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b92e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b92e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b92e-110">Handle de la fenêtre de la page.</span><span class="sxs-lookup"><span data-stu-id="9b92e-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="9b92e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b92e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b92e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9b92e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b92e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b92e-113">Return value</span></span>

<span data-ttu-id="9b92e-114">Retourne l’index de base zéro de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9b92e-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="9b92e-115">Sinon, retourne -1.</span><span class="sxs-lookup"><span data-stu-id="9b92e-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b92e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b92e-116">Requirements</span></span>



| <span data-ttu-id="9b92e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b92e-117">Requirement</span></span> | <span data-ttu-id="9b92e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b92e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b92e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b92e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b92e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b92e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9b92e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b92e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b92e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b92e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9b92e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b92e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b92e-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b92e-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





