---
description: 'Permet à l’objet de rappel de modifier un menu contextuel de l’Explorateur Windows avant qu’il ne soit affiché. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973790"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="5b5ec-104">\_Message SFVM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="5b5ec-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="5b5ec-105">Permet à l’objet de rappel de modifier un menu contextuel de l’Explorateur Windows avant qu’il ne soit affiché.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="5b5ec-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5b5ec-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="5b5ec-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b5ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5ec-108">*idCmd \_ nIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b5ec-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5ec-109">Le mot de poids faible de ce paramètre contient la valeur du premier ID de commande réservé pour les commandes du client.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="5b5ec-110">Le mot de poids fort contient l’index du menu.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="5b5ec-111">*HMENU* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b5ec-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b5ec-112">Handle du menu.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b5ec-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5b5ec-113">Remarks</span></span>

<span data-ttu-id="5b5ec-114">L’objet de vue de dossier système envoie ce message lorsqu’un menu est sélectionné, mais avant son affichage.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="5b5ec-115">Traiter ce message si, par exemple, vous devez activer ou désactiver les commandes de menu.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="5b5ec-116">Le menu contextuel peut être :</span><span class="sxs-lookup"><span data-stu-id="5b5ec-116">The popup menu can be:</span></span>

-   <span data-ttu-id="5b5ec-117">Le menu fichier, modifier ou afficher.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="5b5ec-118">Menu de niveau supérieur défini par le client.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="5b5ec-119">Sous-menu défini par le client.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5ec-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5b5ec-120">Requirements</span></span>



| <span data-ttu-id="5b5ec-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b5ec-121">Requirement</span></span> | <span data-ttu-id="5b5ec-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b5ec-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5ec-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5ec-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5ec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5b5ec-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5ec-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5ec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b5ec-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b5ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5ec-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5ec-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5ec-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b5ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5ec-130">**SFVM \_ MERGEMENU**</span><span class="sxs-lookup"><span data-stu-id="5b5ec-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
