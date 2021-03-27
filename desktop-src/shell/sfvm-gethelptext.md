---
description: 'Permet à l’objet de rappel de spécifier une chaîne de texte d’aide pour les éléments de menu ou les boutons de barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757840"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="132c3-104">\_Message SFVM GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="132c3-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="132c3-105">Permet à l’objet de rappel de spécifier une chaîne de texte d’aide pour les éléments de menu ou les boutons de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="132c3-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="132c3-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="132c3-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="132c3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="132c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="132c3-108">*idCmd \_ cchMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="132c3-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132c3-109">Le mot de poids faible de ce paramètre contient l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="132c3-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="132c3-110">Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .</span><span class="sxs-lookup"><span data-stu-id="132c3-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="132c3-111">*pszText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="132c3-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="132c3-112">Chaîne terminée par le caractère null qui contient le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="132c3-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="132c3-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="132c3-113">Requirements</span></span>



| <span data-ttu-id="132c3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="132c3-114">Requirement</span></span> | <span data-ttu-id="132c3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="132c3-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="132c3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="132c3-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="132c3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="132c3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="132c3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="132c3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="132c3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="132c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="132c3-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="132c3-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
