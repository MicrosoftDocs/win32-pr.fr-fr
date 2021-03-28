---
description: 'Permet à l’objet de rappel de spécifier qu’une animation doit être affichée pendant que les éléments sont énumérés sur un thread d’arrière-plan. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Message SFVM_GETANIMATION (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115834"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="1b00d-104">\_Message SFVM GETANIMATION</span><span class="sxs-lookup"><span data-stu-id="1b00d-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="1b00d-105">Permet à l’objet de rappel de spécifier qu’une animation doit être affichée pendant que les éléments sont énumérés sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1b00d-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="1b00d-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="1b00d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="1b00d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b00d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b00d-108">*phinst* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b00d-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b00d-109">Handle d’instance du module à partir duquel la ressource doit être chargée.</span><span class="sxs-lookup"><span data-stu-id="1b00d-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="1b00d-110">*pwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b00d-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b00d-111">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès du fichier. avi ou le nom d’une ressource AVI.</span><span class="sxs-lookup"><span data-stu-id="1b00d-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="1b00d-112">Ce paramètre peut également être constitué de l’identificateur de ressource dans le mot de poids faible et de 0 dans le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="1b00d-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="1b00d-113">Pour créer cette valeur, utilisez la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="1b00d-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="1b00d-114">Le contrôle charge la ressource à partir du module spécifié par hinst.</span><span class="sxs-lookup"><span data-stu-id="1b00d-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="1b00d-115">Une ressource AVI doit avoir le type « AVI ».</span><span class="sxs-lookup"><span data-stu-id="1b00d-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b00d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1b00d-116">Remarks</span></span>

<span data-ttu-id="1b00d-117">Par défaut, l’objet de vue du dossier système affiche l’animation « torche » pendant une énumération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1b00d-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="1b00d-118">*phinst* et *pwszName* sont passés au contrôle d' [animation](../controls/animation-control-overview.md) avec un message [**ACM \_ ouvert**](../controls/acm-open.md) .</span><span class="sxs-lookup"><span data-stu-id="1b00d-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b00d-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b00d-119">Requirements</span></span>



| <span data-ttu-id="1b00d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b00d-120">Requirement</span></span> | <span data-ttu-id="1b00d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b00d-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b00d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b00d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b00d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b00d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1b00d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b00d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b00d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b00d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b00d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b00d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b00d-127"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b00d-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
