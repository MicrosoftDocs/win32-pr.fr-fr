---
title: Message TB_GETIDEALSIZE (commctrl. h)
description: Obtient la taille idéale de la barre d’outils.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032486"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="bb887-104">TO \_ GETIDEALSIZE message</span><span class="sxs-lookup"><span data-stu-id="bb887-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="bb887-105">Obtient la taille idéale de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bb887-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb887-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb887-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb887-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb887-108">Valeur **booléenne** qui indique s’il faut récupérer la hauteur ou la largeur idéale de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bb887-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="bb887-109">Utilisez **true** pour récupérer la hauteur idéale, **false** pour récupérer la largeur idéale.</span><span class="sxs-lookup"><span data-stu-id="bb887-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="bb887-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb887-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb887-111">Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) qui reçoit la hauteur ou la largeur d’affichage de tous les boutons.</span><span class="sxs-lookup"><span data-stu-id="bb887-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="bb887-112">Si *wParam* a la **valeur true**, seul le membre **CY** (Height) est valide.</span><span class="sxs-lookup"><span data-stu-id="bb887-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="bb887-113">Si *wParam* a la **valeur false**, seul le membre **CX** (Width) est valide.</span><span class="sxs-lookup"><span data-stu-id="bb887-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb887-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb887-114">Return value</span></span>

<span data-ttu-id="bb887-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bb887-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb887-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb887-116">Requirements</span></span>



| <span data-ttu-id="bb887-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb887-117">Requirement</span></span> | <span data-ttu-id="bb887-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb887-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb887-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb887-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb887-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb887-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb887-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb887-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb887-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb887-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb887-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb887-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb887-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb887-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

