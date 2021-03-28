---
description: SFVM \_ DIDDRAGDROP peut être modifié ou non disponible.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Message SFVM_DIDDRAGDROP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991681"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="9d529-103">\_Message SFVM DIDDRAGDROP</span><span class="sxs-lookup"><span data-stu-id="9d529-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="9d529-104">\[**SFVM \_ DIDDRAGDROP** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9d529-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d529-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="9d529-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="9d529-106">Notifie la fonction de rappel qu’une opération de glisser-déplacer a commencé.</span><span class="sxs-lookup"><span data-stu-id="9d529-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="9d529-107">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="9d529-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="9d529-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d529-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d529-109">*dwEffect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d529-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d529-110">Spécificateur d’effet de déplacement de l’énumération [**DROPEFFECT**](../com/dropeffect-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="9d529-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="9d529-111">Cela est obtenu en appelant [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span><span class="sxs-lookup"><span data-stu-id="9d529-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="9d529-112">*pIdo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d529-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d529-113">Pointeur vers l’instance [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="9d529-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d529-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d529-114">Requirements</span></span>



| <span data-ttu-id="9d529-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d529-115">Requirement</span></span> | <span data-ttu-id="9d529-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d529-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d529-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d529-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d529-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d529-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9d529-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d529-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d529-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d529-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d529-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9d529-121">End of client support</span></span><br/>    | <span data-ttu-id="9d529-122">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="9d529-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="9d529-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9d529-123">End of server support</span></span><br/>    | <span data-ttu-id="9d529-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d529-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="9d529-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d529-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d529-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d529-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
