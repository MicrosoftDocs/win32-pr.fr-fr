---
title: Message TB_CHECKBUTTON (commctrl. h)
description: Vérifie ou décoche un bouton donné dans une barre d’outils.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033266"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="0242a-104">TO \_ CHECKBUTTON message</span><span class="sxs-lookup"><span data-stu-id="0242a-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="0242a-105">Vérifie ou décoche un bouton donné dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0242a-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0242a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0242a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0242a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0242a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0242a-108">Identificateur de commande du bouton à vérifier.</span><span class="sxs-lookup"><span data-stu-id="0242a-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="0242a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0242a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0242a-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut activer ou désactiver le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="0242a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="0242a-111">Si la **valeur est true**, la vérification est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0242a-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="0242a-112">Si la **valeur est false**, la vérification est supprimée.</span><span class="sxs-lookup"><span data-stu-id="0242a-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0242a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0242a-113">Return value</span></span>

<span data-ttu-id="0242a-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0242a-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0242a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0242a-115">Remarks</span></span>

<span data-ttu-id="0242a-116">Quand un bouton est activé, il est affiché dans un état appuyé.</span><span class="sxs-lookup"><span data-stu-id="0242a-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0242a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0242a-117">Requirements</span></span>



| <span data-ttu-id="0242a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0242a-118">Requirement</span></span> | <span data-ttu-id="0242a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0242a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0242a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0242a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0242a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0242a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0242a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0242a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0242a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0242a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0242a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0242a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0242a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0242a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

