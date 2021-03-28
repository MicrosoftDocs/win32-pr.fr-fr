---
description: 'Avertit l’objet de rappel qu’un événement a eu lieu et affecte l’un de ses éléments. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_FSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "104991833"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="af8c4-104">\_Message SFVM FSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="af8c4-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="af8c4-105">Avertit l’objet de rappel qu’un événement a eu lieu et affecte l’un de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="af8c4-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="af8c4-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="af8c4-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="af8c4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af8c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8c4-108">*ppidl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af8c4-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af8c4-109">Pointeur de PIDL de l’élément affecté.</span><span class="sxs-lookup"><span data-stu-id="af8c4-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="af8c4-110">*lEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af8c4-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af8c4-111">Valeur SHCNE qui indique l’événement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="af8c4-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="af8c4-112">Pour obtenir la liste des valeurs possibles, consultez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="af8c4-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af8c4-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="af8c4-113">Requirements</span></span>



| <span data-ttu-id="af8c4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af8c4-114">Requirement</span></span> | <span data-ttu-id="af8c4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="af8c4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af8c4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af8c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="af8c4-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af8c4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="af8c4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af8c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="af8c4-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af8c4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af8c4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="af8c4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8c4-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8c4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
