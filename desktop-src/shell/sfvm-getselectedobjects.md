---
description: Récupère un tableau de pointeurs vers des listes d’identificateurs d’élément (PIDL) pour tous les objets sélectionnés. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_GETSELECTEDOBJECTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868697"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="cf773-104">\_Message SFVM GETSELECTEDOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cf773-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="cf773-105">Récupère un tableau de pointeurs vers des listes d’identificateurs d’élément (PIDL) pour tous les objets sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="cf773-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="cf773-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="cf773-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="cf773-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf773-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf773-108">*ppidl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cf773-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="cf773-109">Adresse d’un tableau de PIDL d’objets actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="cf773-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf773-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf773-110">Return value</span></span>

<span data-ttu-id="cf773-111">Retourne le nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="cf773-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf773-112">Notes</span><span class="sxs-lookup"><span data-stu-id="cf773-112">Remarks</span></span>

<span data-ttu-id="cf773-113">Lorsque vous avez terminé, vous devez appeler [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) sur chaque membre du tableau pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="cf773-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf773-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cf773-114">Requirements</span></span>



| <span data-ttu-id="cf773-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf773-115">Requirement</span></span> | <span data-ttu-id="cf773-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf773-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf773-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf773-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf773-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf773-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cf773-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf773-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf773-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf773-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf773-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf773-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf773-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf773-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




