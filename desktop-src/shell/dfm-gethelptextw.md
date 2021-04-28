---
description: 'DFM_GETHELPTEXTW message : permet à l’objet de rappel de spécifier une chaîne de texte d’aide.'
title: Message DFM_GETHELPTEXTW (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097037"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="46e47-103">\_Message DFM GETHELPTEXTW</span><span class="sxs-lookup"><span data-stu-id="46e47-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="46e47-104">Permet à l’objet de rappel de spécifier une chaîne de texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="46e47-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="46e47-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46e47-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e47-106">*idCmd \_ cchMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46e47-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e47-107">Le mot de poids faible de ce paramètre contient l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="46e47-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="46e47-108">Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .</span><span class="sxs-lookup"><span data-stu-id="46e47-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="46e47-109">*pszText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46e47-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e47-110">Chaîne Unicode se terminant par un caractère null qui contient le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="46e47-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46e47-111">Notes </span><span class="sxs-lookup"><span data-stu-id="46e47-111">Remarks</span></span>

<span data-ttu-id="46e47-112">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit.</span><span class="sxs-lookup"><span data-stu-id="46e47-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="46e47-113">Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="46e47-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="46e47-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="46e47-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="46e47-115">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="46e47-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e47-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46e47-116">Requirements</span></span>



| <span data-ttu-id="46e47-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46e47-117">Requirement</span></span> | <span data-ttu-id="46e47-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="46e47-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46e47-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46e47-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46e47-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46e47-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="46e47-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46e47-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46e47-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46e47-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46e47-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="46e47-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46e47-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="46e47-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="46e47-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="46e47-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="46e47-126">**DFM \_ GETHELPTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="46e47-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




