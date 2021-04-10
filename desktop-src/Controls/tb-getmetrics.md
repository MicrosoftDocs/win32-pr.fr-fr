---
title: Message TB_GETMETRICS (commctrl. h)
description: Récupère les métriques d’un contrôle ToolBar.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- TB_GETMETRICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843989"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="b6dbf-104">TO \_ GETMETRICS message</span><span class="sxs-lookup"><span data-stu-id="b6dbf-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="b6dbf-105">Récupère les métriques d’un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6dbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6dbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6dbf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b6dbf-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b6dbf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6dbf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6dbf-110">Pointeur vers une structure [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) qui reçoit les métriques de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6dbf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6dbf-111">Return value</span></span>

<span data-ttu-id="b6dbf-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6dbf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b6dbf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6dbf-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b6dbf-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b6dbf-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6dbf-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6dbf-116">Requirements</span></span>



| <span data-ttu-id="b6dbf-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6dbf-117">Requirement</span></span> | <span data-ttu-id="b6dbf-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6dbf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dbf-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6dbf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6dbf-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6dbf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6dbf-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6dbf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6dbf-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6dbf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6dbf-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6dbf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6dbf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6dbf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





