---
description: Notifie le IShellView quand l’un de ses objets est placé dans le presse-papiers à la suite d’une commande de menu. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_SETCLIPBOARD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991801"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="453ea-104">\_Message SFVM SETCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="453ea-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="453ea-105">Notifie le [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quand l’un de ses objets est placé dans le presse-papiers à la suite d’une commande de menu.</span><span class="sxs-lookup"><span data-stu-id="453ea-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="453ea-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="453ea-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="453ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="453ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453ea-108">*dwEffect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="453ea-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453ea-109">Utilisez (WPARAM)-2 si l’élément est coupé dans le presse-papiers ou (WPARAM)-3 Si l’élément est copié dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="453ea-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="453ea-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="453ea-110">Return value</span></span>

<span data-ttu-id="453ea-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="453ea-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="453ea-112">Notes</span><span class="sxs-lookup"><span data-stu-id="453ea-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="453ea-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="453ea-113">Requirements</span></span>



| <span data-ttu-id="453ea-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="453ea-114">Requirement</span></span> | <span data-ttu-id="453ea-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="453ea-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="453ea-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="453ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="453ea-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="453ea-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="453ea-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="453ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="453ea-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="453ea-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="453ea-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="453ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="453ea-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="453ea-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




