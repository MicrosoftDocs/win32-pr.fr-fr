---
title: Message EM_SEARCHWEB (commctrl. h)
description: Ouvre le navigateur et effectue une recherche sur le Web avec le texte sélectionné comme terme de recherche.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844042"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="06758-104">\_Message SEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="06758-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="06758-105">Ouvre le navigateur et effectue une recherche sur le Web avec le texte sélectionné comme terme de recherche.</span><span class="sxs-lookup"><span data-stu-id="06758-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="06758-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06758-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06758-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06758-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06758-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="06758-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="06758-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06758-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06758-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="06758-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06758-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06758-111">Return value</span></span>

<span data-ttu-id="06758-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="06758-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06758-113">Notes</span><span class="sxs-lookup"><span data-stu-id="06758-113">Remarks</span></span>

<span data-ttu-id="06758-114">Si la fonctionnalité « Rechercher sur le Web » est désactivée à l’aide du message [**\_ ENABLESEARCHWEB em**](em-enablesearchweb.md) , ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="06758-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="06758-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06758-115">Requirements</span></span>



| <span data-ttu-id="06758-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06758-116">Requirement</span></span> | <span data-ttu-id="06758-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="06758-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06758-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06758-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06758-119">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06758-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06758-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06758-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06758-121">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06758-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06758-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="06758-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06758-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06758-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06758-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06758-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06758-125">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="06758-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 





