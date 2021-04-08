---
title: Message SBM_GETSCROLLBARINFO (winuser. h)
description: Envoyé par une application pour récupérer des informations sur la barre de défilement spécifiée.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741373"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="44674-104">\_Message SBM GETSCROLLBARINFO</span><span class="sxs-lookup"><span data-stu-id="44674-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="44674-105">Envoyé par une application pour récupérer des informations sur la barre de défilement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="44674-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="44674-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44674-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44674-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44674-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44674-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="44674-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="44674-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44674-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44674-110">Pointeur vers une structure [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) qui reçoit les informations.</span><span class="sxs-lookup"><span data-stu-id="44674-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44674-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44674-111">Return value</span></span>

<span data-ttu-id="44674-112">Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="44674-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="44674-113">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="44674-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="44674-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44674-114">Requirements</span></span>



| <span data-ttu-id="44674-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44674-115">Requirement</span></span> | <span data-ttu-id="44674-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="44674-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44674-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44674-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44674-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44674-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44674-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44674-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44674-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44674-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44674-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="44674-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44674-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44674-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44674-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44674-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="44674-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="44674-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44674-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="44674-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="44674-126">**SCROLLBARINFO**</span><span class="sxs-lookup"><span data-stu-id="44674-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

