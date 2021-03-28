---
description: SFVM \_ THISIDLIST peut être modifié ou non disponible.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Message SFVM_THISIDLIST (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760197"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="6c9a4-103">\_Message SFVM THISIDLIST</span><span class="sxs-lookup"><span data-stu-id="6c9a4-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="6c9a4-104">\[**SFVM \_ THISIDLIST** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6c9a4-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c9a4-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="6c9a4-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6c9a4-106">Permet à l’objet de rappel de spécifier le pointeur de la vue vers une liste d’identificateurs d’éléments (PIDL).</span><span class="sxs-lookup"><span data-stu-id="6c9a4-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="6c9a4-107">Utilisé uniquement lorsque [**IPersistIDList :: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) et [**IPersistFolder2 :: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) ont échoué.</span><span class="sxs-lookup"><span data-stu-id="6c9a4-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="6c9a4-108">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6c9a4-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="6c9a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c9a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9a4-110">*PIDL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6c9a4-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c9a4-111">Adresse du PIDL de la vue.</span><span class="sxs-lookup"><span data-stu-id="6c9a4-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c9a4-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6c9a4-112">Requirements</span></span>



| <span data-ttu-id="6c9a4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c9a4-113">Requirement</span></span> | <span data-ttu-id="6c9a4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c9a4-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9a4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9a4-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c9a4-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c9a4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c9a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9a4-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c9a4-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c9a4-119">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6c9a4-119">End of client support</span></span><br/>    | <span data-ttu-id="6c9a4-120">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="6c9a4-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="6c9a4-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6c9a4-121">End of server support</span></span><br/>    | <span data-ttu-id="6c9a4-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c9a4-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="6c9a4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c9a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c9a4-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c9a4-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
