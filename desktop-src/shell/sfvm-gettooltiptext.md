---
description: 'Permet à l’objet de rappel de spécifier une chaîne de texte d’info-bulle pour les éléments de menu ou les boutons de barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Message SFVM_GETTOOLTIPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953015"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="1dd2d-104">\_Message SFVM GETTOOLTIPTEXT</span><span class="sxs-lookup"><span data-stu-id="1dd2d-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="1dd2d-105">Permet à l’objet de rappel de spécifier une chaîne de texte d’info-bulle pour les éléments de menu ou les boutons de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="1dd2d-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="1dd2d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="1dd2d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dd2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd2d-108">*idCmd \_ cchMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1dd2d-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd2d-109">Le mot de poids faible de ce paramètre contient l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="1dd2d-110">Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .</span><span class="sxs-lookup"><span data-stu-id="1dd2d-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1dd2d-111">*pszText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1dd2d-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd2d-112">Chaîne terminée par le caractère null qui contient le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dd2d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1dd2d-113">Requirements</span></span>



| <span data-ttu-id="1dd2d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dd2d-114">Requirement</span></span> | <span data-ttu-id="1dd2d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dd2d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd2d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dd2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd2d-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dd2d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1dd2d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dd2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd2d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dd2d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1dd2d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1dd2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd2d-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd2d-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
