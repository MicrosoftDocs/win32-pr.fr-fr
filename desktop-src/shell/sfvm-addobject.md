---
description: Ajoute un objet à la vue de l’interpréteur de commandes. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_ADDOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991668"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="36912-104">\_Message SFVM ADDOBJECT</span><span class="sxs-lookup"><span data-stu-id="36912-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="36912-105">Ajoute un objet à la vue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="36912-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="36912-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="36912-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="36912-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36912-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36912-108">*PIDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36912-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="36912-109">Pointeur vers l’objet d’intérêt à ajouter.</span><span class="sxs-lookup"><span data-stu-id="36912-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36912-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36912-110">Return value</span></span>

<span data-ttu-id="36912-111">Retourne le nouvel ID d’élément ListView de l’objet ajouté si le processus a réussi ; Sinon, retourne-1.</span><span class="sxs-lookup"><span data-stu-id="36912-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="36912-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="36912-112">Requirements</span></span>



| <span data-ttu-id="36912-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36912-113">Requirement</span></span> | <span data-ttu-id="36912-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="36912-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36912-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36912-115">Minimum supported client</span></span><br/> | <span data-ttu-id="36912-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36912-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36912-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36912-117">Minimum supported server</span></span><br/> | <span data-ttu-id="36912-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36912-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36912-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="36912-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="36912-120"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="36912-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




