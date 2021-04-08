---
title: Message TB_SETMETRICS (commctrl. h)
description: Définit les métriques d’un contrôle ToolBar.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- TB_SETMETRICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941844"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="75ca8-104">TO \_ SETMETRICS message</span><span class="sxs-lookup"><span data-stu-id="75ca8-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="75ca8-105">Définit les métriques d’un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="75ca8-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="75ca8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ca8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75ca8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="75ca8-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="75ca8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="75ca8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75ca8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75ca8-110">Structure [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) qui contient les métriques de la barre d’outils à définir.</span><span class="sxs-lookup"><span data-stu-id="75ca8-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ca8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75ca8-111">Return value</span></span>

<span data-ttu-id="75ca8-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="75ca8-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ca8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="75ca8-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75ca8-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="75ca8-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="75ca8-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="75ca8-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75ca8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75ca8-116">Requirements</span></span>



| <span data-ttu-id="75ca8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75ca8-117">Requirement</span></span> | <span data-ttu-id="75ca8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="75ca8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75ca8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75ca8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75ca8-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75ca8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75ca8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75ca8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75ca8-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75ca8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75ca8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="75ca8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ca8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ca8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





