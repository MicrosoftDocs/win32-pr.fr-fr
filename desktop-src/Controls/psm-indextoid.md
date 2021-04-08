---
title: Message PSM_INDEXTOID (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son ID de ressource. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033013"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="8b32a-105">\_Message PSM INDEXTOID</span><span class="sxs-lookup"><span data-stu-id="8b32a-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="8b32a-106">Prend l’index d’une page de feuille de propriétés et retourne son ID de ressource.</span><span class="sxs-lookup"><span data-stu-id="8b32a-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="8b32a-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .</span><span class="sxs-lookup"><span data-stu-id="8b32a-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b32a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b32a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b32a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b32a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b32a-110">Index de base zéro de la page.</span><span class="sxs-lookup"><span data-stu-id="8b32a-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="8b32a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b32a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b32a-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8b32a-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b32a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b32a-113">Return value</span></span>

<span data-ttu-id="8b32a-114">Retourne l’ID de ressource de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="8b32a-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="8b32a-115">Sinon, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="8b32a-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b32a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b32a-116">Requirements</span></span>



| <span data-ttu-id="8b32a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b32a-117">Requirement</span></span> | <span data-ttu-id="8b32a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b32a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b32a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b32a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b32a-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b32a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b32a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b32a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b32a-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b32a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8b32a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b32a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b32a-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b32a-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 





