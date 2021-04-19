---
title: HWINEVENTHOOK (WINDEF. h)
description: Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509106"
---
# <a name="hwineventhook"></a><span data-ttu-id="4c236-104">HWINEVENTHOOK</span><span class="sxs-lookup"><span data-stu-id="4c236-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="4c236-105">Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4c236-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="4c236-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4c236-106">Remarks</span></span>

<span data-ttu-id="4c236-107">Ce type de données est utilisé avec la fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et les fonctions [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) et [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .</span><span class="sxs-lookup"><span data-stu-id="4c236-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c236-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c236-108">Requirements</span></span>



| <span data-ttu-id="4c236-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c236-109">Requirement</span></span> | <span data-ttu-id="4c236-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c236-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c236-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c236-111">Minimum supported client</span></span><br/> | <span data-ttu-id="4c236-112">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c236-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4c236-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c236-113">Minimum supported server</span></span><br/> | <span data-ttu-id="4c236-114">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c236-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="4c236-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4c236-115">Redistributable</span></span><br/>          | <span data-ttu-id="4c236-116">Active Accessibility 1,3 RDK sur Windows NT 4,0 avec SP6 et versions ultérieures et Windows 95</span><span class="sxs-lookup"><span data-stu-id="4c236-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="4c236-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c236-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c236-118"><dt>WINDEF. h (WINVER >= 0x0500) (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c236-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





