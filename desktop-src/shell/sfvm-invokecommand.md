---
description: 'Avertit l’objet de rappel qu’une de ses commandes de menu ou de barre d’outils a été appelée par l’utilisateur. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Message SFVM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868694"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="f92fa-104">\_Message SFVM commande InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="f92fa-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="f92fa-105">Avertit l’objet de rappel qu’une de ses commandes de menu ou de barre d’outils a été appelée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f92fa-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="f92fa-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="f92fa-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="f92fa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f92fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92fa-108">*idCmd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f92fa-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f92fa-109">ID de commande de la barre d’outils ou de l’élément de menu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f92fa-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f92fa-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f92fa-110">Remarks</span></span>

<span data-ttu-id="f92fa-111">Ce message sert essentiellement la même fonction qu’un message de [**\_ commande WM**](../menurc/wm-command.md) dans une procédure de fenêtre conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="f92fa-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="f92fa-112">Elle permet à l’objet de rappel de gérer tous les éléments qu’il a ajoutés à l’outil ou à la barre de menus de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="f92fa-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="f92fa-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f92fa-113">Requirements</span></span>



| <span data-ttu-id="f92fa-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f92fa-114">Requirement</span></span> | <span data-ttu-id="f92fa-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f92fa-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f92fa-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f92fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f92fa-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f92fa-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f92fa-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f92fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f92fa-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f92fa-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f92fa-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f92fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f92fa-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f92fa-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
