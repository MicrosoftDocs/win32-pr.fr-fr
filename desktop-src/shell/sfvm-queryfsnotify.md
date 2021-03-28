---
description: SFVM \_ QUERYFSNOTIFY peut être modifié ou non disponible.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Message SFVM_QUERYFSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210834"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="6700e-103">\_Message SFVM QUERYFSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="6700e-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="6700e-104">\[**SFVM \_ QUERYFSNOTIFY** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6700e-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6700e-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="6700e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6700e-106">Permet à l’objet de rappel d’inscrire un dossier afin que les modifications apportées à la vue de ce dossier génèrent des notifications.</span><span class="sxs-lookup"><span data-stu-id="6700e-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="6700e-107">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6700e-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="6700e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6700e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6700e-109">*shcne* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6700e-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6700e-110">Structure destinée à contenir le PIDL de l’élément pour surveiller les événements et indiquer si les sous-dossiers de cet élément doivent également être surveillés.</span><span class="sxs-lookup"><span data-stu-id="6700e-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6700e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6700e-111">Requirements</span></span>



| <span data-ttu-id="6700e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6700e-112">Requirement</span></span> | <span data-ttu-id="6700e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6700e-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6700e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6700e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6700e-115">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6700e-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6700e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6700e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6700e-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6700e-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6700e-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6700e-118">End of client support</span></span><br/>    | <span data-ttu-id="6700e-119">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="6700e-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="6700e-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6700e-120">End of server support</span></span><br/>    | <span data-ttu-id="6700e-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6700e-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="6700e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6700e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6700e-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6700e-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
