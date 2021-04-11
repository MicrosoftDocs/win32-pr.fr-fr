---
description: Récupère le handle de menu pour la fenêtre active.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Message MN_GETHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202917"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="9d9c8-103">MN \_ message GETHMENU</span><span class="sxs-lookup"><span data-stu-id="9d9c8-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="9d9c8-104">Récupère le handle de menu pour la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="9d9c8-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="9d9c8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d9c8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9c8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d9c8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d9c8-107">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d9c8-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d9c8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d9c8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d9c8-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d9c8-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9c8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d9c8-110">Return value</span></span>

<span data-ttu-id="9d9c8-111">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="9d9c8-111">Type: **HMENU**</span></span>

<span data-ttu-id="9d9c8-112">En cas de réussite, la valeur de retour est **HMENU** pour la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="9d9c8-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="9d9c8-113">En cas d’échec, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="9d9c8-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9c8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d9c8-114">Requirements</span></span>



| <span data-ttu-id="9d9c8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d9c8-115">Requirement</span></span> | <span data-ttu-id="9d9c8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d9c8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9c8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9c8-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9c8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9d9c8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9c8-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9c8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9d9c8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d9c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9c8-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d9c8-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




