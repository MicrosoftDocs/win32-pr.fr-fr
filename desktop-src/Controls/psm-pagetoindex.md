---
title: Message PSM_PAGETOINDEX (Prsht. h)
description: Prend le handle HPROPSHEETPAGE de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513792"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="aa1f3-105">\_Message PSM PAGETOINDEX</span><span class="sxs-lookup"><span data-stu-id="aa1f3-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="aa1f3-106">Prend le handle HPROPSHEETPAGE de la page de la feuille de propriétés et retourne son index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="aa1f3-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="aa1f3-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .</span><span class="sxs-lookup"><span data-stu-id="aa1f3-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa1f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa1f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa1f3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1f3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="aa1f3-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aa1f3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa1f3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa1f3-112">Handle HPROPSHEETPAGE vers la page de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa1f3-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa1f3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa1f3-113">Return value</span></span>

<span data-ttu-id="aa1f3-114">Retourne l’index de base zéro de la page de feuille de propriétés spécifiée par *lParam* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="aa1f3-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="aa1f3-115">Sinon, retourne -1.</span><span class="sxs-lookup"><span data-stu-id="aa1f3-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1f3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa1f3-116">Requirements</span></span>



| <span data-ttu-id="aa1f3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa1f3-117">Requirement</span></span> | <span data-ttu-id="aa1f3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa1f3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1f3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa1f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1f3-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa1f3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aa1f3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa1f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1f3-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa1f3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aa1f3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa1f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa1f3-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa1f3-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





