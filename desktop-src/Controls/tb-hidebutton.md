---
title: Message TB_HIDEBUTTON (commctrl. h)
description: Masque ou affiche le bouton spécifié dans une barre d’outils.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- TB_HIDEBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941948"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="d7e95-104">TO \_ HIDEBUTTON message</span><span class="sxs-lookup"><span data-stu-id="d7e95-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="d7e95-105">Masque ou affiche le bouton spécifié dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d7e95-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7e95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7e95-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e95-108">Identificateur de commande du bouton à masquer ou afficher.</span><span class="sxs-lookup"><span data-stu-id="d7e95-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="d7e95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7e95-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e95-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut masquer ou afficher le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7e95-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="d7e95-111">Si la **valeur est true**, le bouton est masqué.</span><span class="sxs-lookup"><span data-stu-id="d7e95-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="d7e95-112">Si la **valeur est false**, le bouton est affiché.</span><span class="sxs-lookup"><span data-stu-id="d7e95-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="d7e95-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d7e95-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e95-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7e95-114">Return value</span></span>

<span data-ttu-id="d7e95-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d7e95-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e95-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7e95-116">Requirements</span></span>



| <span data-ttu-id="d7e95-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7e95-117">Requirement</span></span> | <span data-ttu-id="d7e95-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7e95-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e95-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e95-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e95-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7e95-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e95-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e95-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7e95-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7e95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e95-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e95-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

