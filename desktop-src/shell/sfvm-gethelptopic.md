---
description: 'Permet à l’objet de rappel de spécifier un fichier d’aide HTML et une rubrique qu’il contient. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETHELPTOPIC (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866778"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="e8bbd-104">\_Message SFVM GETHELPTOPIC</span><span class="sxs-lookup"><span data-stu-id="e8bbd-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="e8bbd-105">Permet à l’objet de rappel de spécifier un fichier d’aide HTML et une rubrique qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="e8bbd-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="e8bbd-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e8bbd-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="e8bbd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8bbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bbd-108">*phtd* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8bbd-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bbd-109">Adresse d’une structure [**de \_ \_ données SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) qui spécifie le fichier d’aide HTML et la rubrique.</span><span class="sxs-lookup"><span data-stu-id="e8bbd-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8bbd-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e8bbd-110">Requirements</span></span>



| <span data-ttu-id="e8bbd-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8bbd-111">Requirement</span></span> | <span data-ttu-id="e8bbd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8bbd-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bbd-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8bbd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e8bbd-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8bbd-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8bbd-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8bbd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e8bbd-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8bbd-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8bbd-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8bbd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8bbd-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8bbd-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
