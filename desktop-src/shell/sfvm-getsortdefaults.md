---
description: 'Permet à l’objet de rappel de spécifier un paramètre de tri par défaut. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETSORTDEFAULTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973814"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="6e85e-104">\_Message SFVM GETSORTDEFAULTS</span><span class="sxs-lookup"><span data-stu-id="6e85e-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="6e85e-105">Permet à l’objet de rappel de spécifier un paramètre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e85e-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="6e85e-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6e85e-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="6e85e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e85e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e85e-108">*iDirection* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e85e-109">Sens de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e85e-109">The default sorting direction.</span></span> <span data-ttu-id="6e85e-110">Définissez ce paramètre sur une valeur positive pour effectuer un tri dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="6e85e-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="6e85e-111">Définissez ce paramètre sur zéro ou sur une valeur négative pour effectuer un tri dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="6e85e-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="6e85e-112">*IColumn* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e85e-113">Colonne utilisée pour le tri.</span><span class="sxs-lookup"><span data-stu-id="6e85e-113">The column used for the sort.</span></span> <span data-ttu-id="6e85e-114">Ce sera passé à [**IShellFolder :: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) dans les 16 bits inférieurs de sa valeur *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6e85e-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e85e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6e85e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e85e-116">: **SFVM \_ GETSORTDEFAULTS** n’est pas reconnu par l’objet de vue de dossier système.</span><span class="sxs-lookup"><span data-stu-id="6e85e-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e85e-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6e85e-117">Requirements</span></span>



| <span data-ttu-id="6e85e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e85e-118">Requirement</span></span> | <span data-ttu-id="6e85e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e85e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e85e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e85e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e85e-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6e85e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e85e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e85e-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e85e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e85e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e85e-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e85e-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
