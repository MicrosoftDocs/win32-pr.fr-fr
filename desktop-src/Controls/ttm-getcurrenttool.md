---
title: Message TTM_GETCURRENTTOOL (commctrl. h)
description: Récupère les informations de l’outil en cours dans un contrôle ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942150"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="d07e3-104">\_Message atténuation GETCURRENTTOOL</span><span class="sxs-lookup"><span data-stu-id="d07e3-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="d07e3-105">Récupère les informations de l’outil en cours dans un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d07e3-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d07e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d07e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d07e3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d07e3-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d07e3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d07e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d07e3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d07e3-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui reçoit des informations sur l’outil en cours.</span><span class="sxs-lookup"><span data-stu-id="d07e3-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="d07e3-111">Si cette valeur est **null**, la valeur de retour indique l’existence de l’outil actuel sans récupérer réellement les informations de l’outil.</span><span class="sxs-lookup"><span data-stu-id="d07e3-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="d07e3-112">Si cette valeur n’est pas **null**, le membre **cbSize** de la structure **TOOLINFO** doit être rempli avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="d07e3-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d07e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d07e3-113">Return value</span></span>

<span data-ttu-id="d07e3-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d07e3-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d07e3-115">Si *lParam* a la **valeur null**, retourne une valeur différente de zéro si un outil en cours existe, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d07e3-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07e3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d07e3-116">Requirements</span></span>



| <span data-ttu-id="d07e3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d07e3-117">Requirement</span></span> | <span data-ttu-id="d07e3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d07e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d07e3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d07e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d07e3-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d07e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d07e3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d07e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d07e3-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d07e3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d07e3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d07e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d07e3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d07e3-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d07e3-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d07e3-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d07e3-126">**Atténuation \_ GETCURRENTTOOLW** (Unicode) et **atténuation \_ GETCURRENTTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d07e3-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





