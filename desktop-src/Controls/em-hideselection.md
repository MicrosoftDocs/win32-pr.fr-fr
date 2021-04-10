---
title: Message EM_HIDESELECTION (RichEdit. h)
description: Le \_ message em HIDESELECTION masque ou affiche la sélection dans un contrôle RichEdit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941740"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="dda57-104">\_Message em HIDESELECTION</span><span class="sxs-lookup"><span data-stu-id="dda57-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="dda57-105">Le message **em \_ HIDESELECTION** masque ou affiche la sélection dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="dda57-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dda57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dda57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda57-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dda57-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dda57-108">Valeur spécifiant s’il faut masquer ou afficher la sélection.</span><span class="sxs-lookup"><span data-stu-id="dda57-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="dda57-109">Si ce paramètre est égal à zéro, la sélection est affichée.</span><span class="sxs-lookup"><span data-stu-id="dda57-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="dda57-110">Dans le cas contraire, la sélection est masquée.</span><span class="sxs-lookup"><span data-stu-id="dda57-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="dda57-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dda57-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dda57-112">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dda57-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda57-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dda57-113">Return value</span></span>

<span data-ttu-id="dda57-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dda57-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda57-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dda57-115">Requirements</span></span>



| <span data-ttu-id="dda57-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dda57-116">Requirement</span></span> | <span data-ttu-id="dda57-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dda57-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dda57-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dda57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dda57-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dda57-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dda57-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dda57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dda57-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dda57-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dda57-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dda57-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda57-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda57-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





