---
description: 'Avertit l’objet de rappel que la fenêtre d’affichage des dossiers est en cours de création. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_WINDOWCREATED (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973806"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="0f3fe-104">\_Message SFVM WINDOWCREATED</span><span class="sxs-lookup"><span data-stu-id="0f3fe-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="0f3fe-105">Avertit l’objet de rappel que la fenêtre d’affichage des dossiers est en cours de création.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="0f3fe-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0f3fe-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="0f3fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f3fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3fe-108">*hwndView* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3fe-109">Handle de fenêtre de la vue du dossier.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f3fe-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0f3fe-110">Requirements</span></span>



| <span data-ttu-id="0f3fe-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f3fe-111">Requirement</span></span> | <span data-ttu-id="0f3fe-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f3fe-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3fe-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3fe-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3fe-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f3fe-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3fe-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3fe-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f3fe-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f3fe-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3fe-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3fe-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
