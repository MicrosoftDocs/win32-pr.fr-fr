---
title: Message TB_SETSTATE (commctrl. h)
description: Définit l’état du bouton spécifié dans une barre d’outils.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106588"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="d1e13-104">TO ( \_ message SETSTATE)</span><span class="sxs-lookup"><span data-stu-id="d1e13-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="d1e13-105">Définit l’état du bouton spécifié dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d1e13-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1e13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1e13-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e13-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="d1e13-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="d1e13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1e13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e13-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est une combinaison de valeurs figurant dans les États des boutons de la [barre d’outils](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="d1e13-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="d1e13-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d1e13-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e13-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1e13-112">Return value</span></span>

<span data-ttu-id="d1e13-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d1e13-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e13-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1e13-114">Requirements</span></span>



| <span data-ttu-id="d1e13-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1e13-115">Requirement</span></span> | <span data-ttu-id="d1e13-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1e13-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e13-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e13-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e13-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1e13-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1e13-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e13-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e13-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1e13-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1e13-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1e13-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e13-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e13-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

