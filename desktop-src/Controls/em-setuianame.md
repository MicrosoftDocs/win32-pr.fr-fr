---
title: Message EM_SETUIANAME (RichEdit. h)
description: Définit le nom d’un contrôle RichEdit pour UI Automation (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942294"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="1de2f-104">\_Message SETUIANAME em</span><span class="sxs-lookup"><span data-stu-id="1de2f-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="1de2f-105">Définit le nom d’un contrôle RichEdit pour UI Automation (UIA).</span><span class="sxs-lookup"><span data-stu-id="1de2f-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="1de2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1de2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de2f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1de2f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de2f-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1de2f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1de2f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1de2f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de2f-110">Pointeur vers la chaîne de nom se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="1de2f-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de2f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1de2f-111">Return value</span></span>

<span data-ttu-id="1de2f-112">TRUE si le nom de UIA est correctement défini ; sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="1de2f-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de2f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1de2f-113">Requirements</span></span>



| <span data-ttu-id="1de2f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1de2f-114">Requirement</span></span> | <span data-ttu-id="1de2f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1de2f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1de2f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de2f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1de2f-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de2f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1de2f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de2f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1de2f-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de2f-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1de2f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1de2f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de2f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1de2f-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





