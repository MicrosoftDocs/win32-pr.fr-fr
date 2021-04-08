---
title: Message MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtient des informations sur une grille de calendrier.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743996"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="8b98b-104">\_Message GETCALENDARGRIDINFO MCM</span><span class="sxs-lookup"><span data-stu-id="8b98b-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="8b98b-105">Obtient des informations sur une grille de calendrier.</span><span class="sxs-lookup"><span data-stu-id="8b98b-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b98b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b98b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b98b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b98b-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8b98b-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8b98b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b98b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b98b-110">Pointeur vers une structure [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) qui contient des informations sur la grille du calendrier.</span><span class="sxs-lookup"><span data-stu-id="8b98b-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b98b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b98b-111">Return value</span></span>

<span data-ttu-id="8b98b-112">**True** en cas de réussite ; sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8b98b-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b98b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b98b-113">Requirements</span></span>



| <span data-ttu-id="8b98b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b98b-114">Requirement</span></span> | <span data-ttu-id="8b98b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b98b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b98b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b98b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b98b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b98b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b98b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b98b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b98b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b98b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b98b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b98b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b98b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b98b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





