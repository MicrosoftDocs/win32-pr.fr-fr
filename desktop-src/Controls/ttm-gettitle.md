---
title: Message TTM_GETTITLE (commctrl. h)
description: Récupérez les informations relatives au titre d’un contrôle ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942146"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="fd1df-104">\_Message atténuation GETTITLE</span><span class="sxs-lookup"><span data-stu-id="fd1df-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="fd1df-105">Récupérez les informations relatives au titre d’un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="fd1df-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd1df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd1df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd1df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd1df-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fd1df-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fd1df-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fd1df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd1df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd1df-110">Pointeur vers une structure [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) qui contient des informations sur un titre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="fd1df-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd1df-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd1df-111">Return value</span></span>

<span data-ttu-id="fd1df-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd1df-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd1df-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fd1df-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd1df-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="fd1df-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fd1df-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd1df-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd1df-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd1df-116">Requirements</span></span>



| <span data-ttu-id="fd1df-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd1df-117">Requirement</span></span> | <span data-ttu-id="fd1df-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd1df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1df-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd1df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1df-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd1df-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd1df-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd1df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1df-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd1df-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd1df-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd1df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1df-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1df-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





