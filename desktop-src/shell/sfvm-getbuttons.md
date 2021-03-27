---
description: 'Permet à l’objet de rappel de spécifier les boutons à ajouter à la barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Message SFVM_GETBUTTONS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866781"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="7e41d-104">\_Message SFVM GETBUTTONS</span><span class="sxs-lookup"><span data-stu-id="7e41d-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="7e41d-105">Permet à l’objet de rappel de spécifier les boutons à ajouter à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="7e41d-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="7e41d-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="7e41d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="7e41d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e41d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e41d-108">*idCmdFirst \_ cbtnMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e41d-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e41d-109">Contient les valeurs 2 16 bits compressées dans le paramètre avec la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) .</span><span class="sxs-lookup"><span data-stu-id="7e41d-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="7e41d-110">Le mot de poids faible contient l’ID de commande initial.</span><span class="sxs-lookup"><span data-stu-id="7e41d-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="7e41d-111">Le mot de poids fort contient le nombre de boutons à ajouter, comme spécifié dans le message [**\_ GETBUTTONINFO SFVM**](sfvm-getbuttoninfo.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="7e41d-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="7e41d-112">*pbtn* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e41d-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e41d-113">Adresse d’un tableau de structures [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , une pour chaque bouton à ajouter à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="7e41d-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e41d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7e41d-114">Remarks</span></span>

<span data-ttu-id="7e41d-115">Ce message est précédé d’un message [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7e41d-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="7e41d-116">L’objet de rappel doit gérer ce message pour spécifier le nombre de boutons et l’emplacement où ils doivent être placés dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="7e41d-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="7e41d-117">En fonction de la façon dont l’objet de rappel répond au message **SFVM \_ GETBUTTONINFO** , les boutons spécifiés par le paramètre *pbtn* seront ajoutés ou ajoutés aux boutons standard de l’objet d’affichage des dossiers système ou remplacent le jeu standard.</span><span class="sxs-lookup"><span data-stu-id="7e41d-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e41d-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7e41d-118">Requirements</span></span>



| <span data-ttu-id="7e41d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e41d-119">Requirement</span></span> | <span data-ttu-id="7e41d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e41d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e41d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e41d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e41d-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e41d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7e41d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e41d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e41d-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e41d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7e41d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e41d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e41d-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e41d-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
