---
description: 'Permet à l’objet de rappel de spécifier le nombre d’éléments dans l’affichage des dossiers. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_DEFITEMCOUNT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952243"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="8407f-104">\_Message SFVM DEFITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="8407f-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="8407f-105">Permet à l’objet de rappel de spécifier le nombre d’éléments dans l’affichage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="8407f-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="8407f-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8407f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="8407f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8407f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8407f-108">*CItems* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8407f-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8407f-109">Nombre d’éléments dans l’affichage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="8407f-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8407f-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8407f-110">Requirements</span></span>



| <span data-ttu-id="8407f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8407f-111">Requirement</span></span> | <span data-ttu-id="8407f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8407f-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8407f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8407f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8407f-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8407f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8407f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8407f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8407f-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8407f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8407f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="8407f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8407f-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8407f-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
