---
title: Message TB_INDETERMINATE (commctrl. h)
description: Définit ou efface l’état indéterminé du bouton spécifié dans une barre d’outils.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032685"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="3cbe7-104">TO \_ message indéterminé</span><span class="sxs-lookup"><span data-stu-id="3cbe7-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="3cbe7-105">Définit ou efface l’état indéterminé du bouton spécifié dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cbe7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cbe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cbe7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cbe7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbe7-108">Identificateur de commande du bouton dont l’état indéterminé doit être défini ou effacé.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="3cbe7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cbe7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbe7-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut définir ou désélectionner l’état indéterminé.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="3cbe7-111">Si la **valeur est true**, l’état indéterminé est défini.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="3cbe7-112">Si la **valeur est false**, l’État est effacé.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="3cbe7-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cbe7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cbe7-114">Return value</span></span>

<span data-ttu-id="3cbe7-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3cbe7-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbe7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cbe7-116">Requirements</span></span>



| <span data-ttu-id="3cbe7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cbe7-117">Requirement</span></span> | <span data-ttu-id="3cbe7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cbe7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbe7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cbe7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3cbe7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cbe7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cbe7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cbe7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3cbe7-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cbe7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cbe7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cbe7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cbe7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cbe7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

