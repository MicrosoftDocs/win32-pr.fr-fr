---
description: 'Avertit l’objet de rappel du site de conteneur. Utilisé uniquement quand IObjectWithSite :: SetSite n’est pas pris en charge et SHCreateShellFolderViewEx est utilisé. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Message SFVM_SETISFV (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973811"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="fd58c-105">\_Message SFVM SETISFV</span><span class="sxs-lookup"><span data-stu-id="fd58c-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="fd58c-106">\[Cette notification est prise en charge via Windows XP Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fd58c-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="fd58c-107">Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd58c-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fd58c-108">Avertit l’objet de rappel du site de conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd58c-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="fd58c-109">Utilisé uniquement quand [**IObjectWithSite :: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) n’est pas pris en charge et [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fd58c-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="fd58c-110">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="fd58c-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="fd58c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd58c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd58c-112">*site* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd58c-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd58c-113">Pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du site conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd58c-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd58c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd58c-114">Requirements</span></span>



| <span data-ttu-id="fd58c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd58c-115">Requirement</span></span> | <span data-ttu-id="fd58c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd58c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd58c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd58c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd58c-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd58c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fd58c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd58c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd58c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd58c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd58c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd58c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd58c-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd58c-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
