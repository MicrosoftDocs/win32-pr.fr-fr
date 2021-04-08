---
title: Message LM_HITTEST (commctrl. h)
description: Détermine si l’utilisateur a cliqué sur le lien spécifié.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843101"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="b882e-104">\_Message LM HITTEST</span><span class="sxs-lookup"><span data-stu-id="b882e-104">LM\_HITTEST message</span></span>

<span data-ttu-id="b882e-105">Détermine si l’utilisateur a cliqué sur le lien spécifié.</span><span class="sxs-lookup"><span data-stu-id="b882e-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="b882e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b882e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b882e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b882e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b882e-108">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b882e-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="b882e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b882e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b882e-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> à remplir avec des informations sur le lien sur lequel l’utilisateur a cliqué, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b882e-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b882e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b882e-111">Return value</span></span>

<span data-ttu-id="b882e-112">Retourne la **valeur true** si l’utilisateur a cliqué sur un lien ; sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b882e-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b882e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b882e-113">Remarks</span></span>

<span data-ttu-id="b882e-114">Si le message **LM \_ HITTEST** est correctement exécuté, le système se remplit en [**litem. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) et en **litem. szID**.</span><span class="sxs-lookup"><span data-stu-id="b882e-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="b882e-115">Si le message **LM \_ HITTEST** échoue, ne supposez pas que toutes les informations contenues dans **litem** sont valides.</span><span class="sxs-lookup"><span data-stu-id="b882e-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="b882e-116">Pour utiliser cette API, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="b882e-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b882e-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b882e-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b882e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b882e-118">Requirements</span></span>



| <span data-ttu-id="b882e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b882e-119">Requirement</span></span> | <span data-ttu-id="b882e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b882e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b882e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b882e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b882e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b882e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b882e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b882e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b882e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b882e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b882e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b882e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b882e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b882e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





