---
description: 'Permet à l’objet de rappel de fournir des informations sur la zone Internet. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Message SFVM_GETZONE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530183"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="4bb4f-104">\_Message SFVM GETZONE</span><span class="sxs-lookup"><span data-stu-id="4bb4f-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="4bb4f-105">\[Cette notification est prise en charge via Windows XP Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="4bb4f-106">Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4bb4f-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4bb4f-107">Permet à l’objet de rappel de fournir des informations sur la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="4bb4f-108">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="4bb4f-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="4bb4f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bb4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb4f-110">*zone* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4bb4f-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb4f-111">L’une des valeurs suivantes indiquant la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="4bb4f-112">Ces valeurs constituent l’énumération [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , définie dans urlmon. h.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="4bb4f-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_ordinateur local \_ URLZONE**</span><span class="sxs-lookup"><span data-stu-id="4bb4f-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="4bb4f-114">Zone utilisée pour le contenu qui se trouve déjà sur l’ordinateur local de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="4bb4f-115">Cette zone n’est pas exposée par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="4bb4f-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_Intranet URLZONE**</span><span class="sxs-lookup"><span data-stu-id="4bb4f-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="4bb4f-117">Zone utilisée pour le contenu trouvé sur un intranet.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="4bb4f-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ approuvé**</span><span class="sxs-lookup"><span data-stu-id="4bb4f-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="4bb4f-119">Zone utilisée pour les sites Web de confiance sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="4bb4f-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="4bb4f-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="4bb4f-121">Zone utilisée pour la majeure partie du contenu sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="4bb4f-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ non approuvé**</span><span class="sxs-lookup"><span data-stu-id="4bb4f-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="4bb4f-123">Zone utilisée pour les sites Web qui ne sont pas approuvés.</span><span class="sxs-lookup"><span data-stu-id="4bb4f-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bb4f-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4bb4f-124">Requirements</span></span>



| <span data-ttu-id="4bb4f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bb4f-125">Requirement</span></span> | <span data-ttu-id="4bb4f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bb4f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb4f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bb4f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb4f-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bb4f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4bb4f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bb4f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb4f-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bb4f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4bb4f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bb4f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bb4f-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb4f-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
