---
description: Supprime un objet de la vue de l’interpréteur de commandes. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_REMOVEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973815"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="eec48-104">\_Message SFVM REMOVEOBJECT</span><span class="sxs-lookup"><span data-stu-id="eec48-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="eec48-105">Supprime un objet de la vue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="eec48-105">Removes an object from the shell view.</span></span> <span data-ttu-id="eec48-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="eec48-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="eec48-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec48-108">*PIDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eec48-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="eec48-109">PIDL de l’objet à supprimer.</span><span class="sxs-lookup"><span data-stu-id="eec48-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec48-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eec48-110">Return value</span></span>

<span data-ttu-id="eec48-111">Retourne l’index de l’élément qui a été supprimé si un élément correspondant au PIDL spécifié a été trouvé ; Sinon, retourne-1.</span><span class="sxs-lookup"><span data-stu-id="eec48-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec48-112">Notes</span><span class="sxs-lookup"><span data-stu-id="eec48-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="eec48-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eec48-113">Requirements</span></span>



| <span data-ttu-id="eec48-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eec48-114">Requirement</span></span> | <span data-ttu-id="eec48-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="eec48-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eec48-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec48-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eec48-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eec48-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eec48-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eec48-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eec48-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eec48-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eec48-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="eec48-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec48-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec48-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




