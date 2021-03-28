---
description: 'Permet à l’objet de rappel de spécifier le mode d’affichage. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_DEFVIEWMODE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991777"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="42003-104">\_Message SFVM DEFVIEWMODE</span><span class="sxs-lookup"><span data-stu-id="42003-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="42003-105">Permet à l’objet de rappel de spécifier le mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="42003-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="42003-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="42003-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="42003-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42003-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42003-108">*pViewMode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42003-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42003-109">L’une des valeurs du type énuméré [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .</span><span class="sxs-lookup"><span data-stu-id="42003-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42003-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42003-110">Requirements</span></span>



| <span data-ttu-id="42003-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42003-111">Requirement</span></span> | <span data-ttu-id="42003-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="42003-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42003-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42003-113">Minimum supported client</span></span><br/> | <span data-ttu-id="42003-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42003-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42003-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42003-115">Minimum supported server</span></span><br/> | <span data-ttu-id="42003-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42003-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="42003-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="42003-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="42003-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="42003-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
