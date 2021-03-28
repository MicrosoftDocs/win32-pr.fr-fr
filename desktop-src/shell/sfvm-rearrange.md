---
description: Notifie le IShellView de réorganiser ses éléments. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_REARRANGE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042784"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="130ca-104">SFVM \_ RÉorganiser le message</span><span class="sxs-lookup"><span data-stu-id="130ca-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="130ca-105">Notifie le [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) de réorganiser ses éléments.</span><span class="sxs-lookup"><span data-stu-id="130ca-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="130ca-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="130ca-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="130ca-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="130ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="130ca-108">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="130ca-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="130ca-109">Passé à [**IShellFolder :: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span><span class="sxs-lookup"><span data-stu-id="130ca-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="130ca-110">Pour plus d’informations sur ce paramètre, consultez [**IShellFolder :: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .</span><span class="sxs-lookup"><span data-stu-id="130ca-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="130ca-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="130ca-111">Return value</span></span>

<span data-ttu-id="130ca-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="130ca-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="130ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="130ca-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="130ca-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="130ca-114">Requirements</span></span>



| <span data-ttu-id="130ca-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="130ca-115">Requirement</span></span> | <span data-ttu-id="130ca-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="130ca-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="130ca-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130ca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="130ca-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="130ca-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="130ca-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130ca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="130ca-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="130ca-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="130ca-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="130ca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="130ca-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="130ca-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




