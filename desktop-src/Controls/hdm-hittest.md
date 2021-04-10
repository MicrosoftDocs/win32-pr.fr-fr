---
title: Message HDM_HITTEST (commctrl. h)
description: Teste un point pour déterminer l’élément d’en-tête, le cas échéant, à l’emplacement spécifié.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104482"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="01ae8-104">\_Message HDM HITTEST</span><span class="sxs-lookup"><span data-stu-id="01ae8-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="01ae8-105">Teste un point pour déterminer l’élément d’en-tête, le cas échéant, à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="01ae8-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="01ae8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01ae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ae8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01ae8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="01ae8-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="01ae8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="01ae8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01ae8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01ae8-110">Pointeur vers une structure [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) qui contient la position à tester et reçoit des informations sur les résultats du test.</span><span class="sxs-lookup"><span data-stu-id="01ae8-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ae8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01ae8-111">Return value</span></span>

<span data-ttu-id="01ae8-112">Retourne l’index de l’élément à la position spécifiée, le cas échéant, ou 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="01ae8-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ae8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01ae8-113">Requirements</span></span>



| <span data-ttu-id="01ae8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01ae8-114">Requirement</span></span> | <span data-ttu-id="01ae8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="01ae8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01ae8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01ae8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01ae8-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01ae8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01ae8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01ae8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01ae8-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01ae8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01ae8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="01ae8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ae8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ae8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





