---
description: Définit la position d’un élément dans la vue de l’interpréteur de commandes. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_SETITEMPOS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210630"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="18ece-104">\_Message SFVM SETITEMPOS</span><span class="sxs-lookup"><span data-stu-id="18ece-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="18ece-105">Définit la position d’un élément dans la vue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="18ece-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="18ece-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="18ece-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="18ece-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18ece-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ece-108">*SIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18ece-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18ece-109">Pointeur vers une structure [**SFV \_ SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .</span><span class="sxs-lookup"><span data-stu-id="18ece-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18ece-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="18ece-110">Requirements</span></span>



| <span data-ttu-id="18ece-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18ece-111">Requirement</span></span> | <span data-ttu-id="18ece-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="18ece-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18ece-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ece-113">Minimum supported client</span></span><br/> | <span data-ttu-id="18ece-114">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18ece-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="18ece-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ece-115">Minimum supported server</span></span><br/> | <span data-ttu-id="18ece-116">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18ece-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="18ece-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="18ece-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ece-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ece-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




