---
description: 'Permet à l’objet de rappel de demander l’énumération sur un thread d’arrière-plan. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_BACKGROUNDENUM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991684"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="bf902-104">\_Message SFVM BACKGROUNDENUM</span><span class="sxs-lookup"><span data-stu-id="bf902-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="bf902-105">Permet à l’objet de rappel de demander l’énumération sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bf902-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="bf902-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="bf902-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="bf902-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf902-107">Parameters</span></span>

<span data-ttu-id="bf902-108">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="bf902-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf902-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bf902-109">Remarks</span></span>

<span data-ttu-id="bf902-110">En réponse à cette notification, retournez \_ OK pour activer l’énumération d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bf902-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="bf902-111">Par défaut, l’objet dossier système affiche l’animation « torche » pendant que l’énumération a lieu.</span><span class="sxs-lookup"><span data-stu-id="bf902-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="bf902-112">Pour spécifier une animation personnalisée, gérez [**SFVM \_ GETANIMATION**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="bf902-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf902-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf902-113">Requirements</span></span>



| <span data-ttu-id="bf902-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf902-114">Requirement</span></span> | <span data-ttu-id="bf902-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf902-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bf902-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf902-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf902-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf902-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bf902-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf902-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf902-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf902-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bf902-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf902-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf902-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf902-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
