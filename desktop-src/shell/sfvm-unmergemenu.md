---
description: 'Avertit l’objet de rappel qu’un menu est en cours de suppression. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_UNMERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973779"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="67381-104">\_Message SFVM UNMERGEMENU</span><span class="sxs-lookup"><span data-stu-id="67381-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="67381-105">Avertit l’objet de rappel qu’un menu est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="67381-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="67381-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="67381-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="67381-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67381-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67381-108">*hmenuCurrent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67381-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67381-109">Handle du menu en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="67381-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67381-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="67381-110">Requirements</span></span>



| <span data-ttu-id="67381-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67381-111">Requirement</span></span> | <span data-ttu-id="67381-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="67381-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67381-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67381-113">Minimum supported client</span></span><br/> | <span data-ttu-id="67381-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67381-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="67381-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67381-115">Minimum supported server</span></span><br/> | <span data-ttu-id="67381-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67381-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="67381-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="67381-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="67381-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="67381-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
