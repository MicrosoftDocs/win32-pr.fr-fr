---
title: Message PSM_INDEXTOPAGE (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466323"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="2a293-105">\_Message PSM INDEXTOPAGE</span><span class="sxs-lookup"><span data-stu-id="2a293-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="2a293-106">Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE.</span><span class="sxs-lookup"><span data-stu-id="2a293-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="2a293-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .</span><span class="sxs-lookup"><span data-stu-id="2a293-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a293-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a293-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a293-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a293-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a293-110">Index de base zéro de la page.</span><span class="sxs-lookup"><span data-stu-id="2a293-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="2a293-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a293-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a293-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2a293-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a293-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a293-113">Return value</span></span>

<span data-ttu-id="2a293-114">Retourne le handle HPROPSHEETPAGE de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2a293-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="2a293-115">Sinon, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2a293-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a293-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a293-116">Requirements</span></span>



| <span data-ttu-id="2a293-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a293-117">Requirement</span></span> | <span data-ttu-id="2a293-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a293-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a293-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a293-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a293-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a293-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2a293-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a293-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a293-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a293-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a293-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a293-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a293-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a293-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





