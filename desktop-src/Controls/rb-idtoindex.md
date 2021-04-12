---
title: Message RB_IDTOINDEX (commctrl. h)
description: Convertit un identificateur de bande en un index de bande dans un contrôle rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464394"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="fea41-104">\_Message IDTOINDEX RB</span><span class="sxs-lookup"><span data-stu-id="fea41-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="fea41-105">Convertit un identificateur de bande en un index de bande dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="fea41-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fea41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fea41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fea41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea41-108">Identificateur défini par l’application de la bande en question.</span><span class="sxs-lookup"><span data-stu-id="fea41-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="fea41-109">Il s’agit de la valeur qui a été transmise dans le membre **wID** de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) lorsque la bande a été insérée.</span><span class="sxs-lookup"><span data-stu-id="fea41-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="fea41-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fea41-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fea41-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fea41-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea41-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fea41-112">Return value</span></span>

<span data-ttu-id="fea41-113">Retourne l’index de la bande de base zéro en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fea41-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="fea41-114">S’il existe des identificateurs de bande en double, le premier est retourné.</span><span class="sxs-lookup"><span data-stu-id="fea41-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea41-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fea41-115">Requirements</span></span>



| <span data-ttu-id="fea41-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fea41-116">Requirement</span></span> | <span data-ttu-id="fea41-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fea41-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fea41-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fea41-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fea41-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fea41-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fea41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fea41-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fea41-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fea41-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fea41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea41-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea41-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





