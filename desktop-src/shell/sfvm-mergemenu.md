---
description: 'Permet à l’objet de rappel de fusionner les éléments de menu dans les menus de l’Explorateur Windows. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_MERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973787"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="d5af4-104">\_Message SFVM MERGEMENU</span><span class="sxs-lookup"><span data-stu-id="d5af4-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="d5af4-105">Permet à l’objet de rappel de fusionner les éléments de menu dans les menus de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d5af4-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="d5af4-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d5af4-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="d5af4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5af4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5af4-108">*pinfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5af4-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5af4-109">Structure [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenant les informations nécessaires pour fusionner les éléments dans le menu.</span><span class="sxs-lookup"><span data-stu-id="d5af4-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5af4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d5af4-110">Remarks</span></span>

<span data-ttu-id="d5af4-111">Ce message remplit essentiellement les mêmes fonctions que [**IShellBrowser :: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) et [**IShellBrowser :: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) dans un affichage de dossier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d5af4-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="d5af4-112">Pour plus d’informations, consultez la section *utilisation de IShellBrowser pour communiquer avec l’Explorateur Windows* de l’article [implémentation d’un affichage des dossiers](../lwef/nse-folderview.md) .</span><span class="sxs-lookup"><span data-stu-id="d5af4-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5af4-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d5af4-113">Requirements</span></span>



| <span data-ttu-id="d5af4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5af4-114">Requirement</span></span> | <span data-ttu-id="d5af4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5af4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5af4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5af4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d5af4-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5af4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d5af4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5af4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d5af4-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5af4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d5af4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5af4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5af4-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5af4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
