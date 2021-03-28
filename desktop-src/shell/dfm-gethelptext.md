---
description: Permet à l’objet de rappel de spécifier une chaîne de texte d’aide.
title: Message DFM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9aefb1c3a12ff00294ccc536464794a17fccfc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525365"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="4a968-103">\_Message DFM GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="4a968-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="4a968-104">Permet à l’objet de rappel de spécifier une chaîne de texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="4a968-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="4a968-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a968-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a968-106">*idCmd \_ cchMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a968-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a968-107">Le mot de poids faible de ce paramètre contient l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="4a968-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="4a968-108">Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .</span><span class="sxs-lookup"><span data-stu-id="4a968-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4a968-109">*pszText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a968-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a968-110">Chaîne ANSI se terminant par un caractère null qui contient le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="4a968-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a968-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4a968-111">Remarks</span></span>

<span data-ttu-id="4a968-112">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit.</span><span class="sxs-lookup"><span data-stu-id="4a968-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="4a968-113">Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="4a968-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="4a968-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="4a968-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="4a968-115">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="4a968-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a968-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a968-116">Requirements</span></span>



| <span data-ttu-id="4a968-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a968-117">Requirement</span></span> | <span data-ttu-id="4a968-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a968-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a968-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a968-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a968-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a968-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a968-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a968-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a968-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a968-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a968-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a968-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a968-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a968-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="4a968-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4a968-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4a968-126">**DFM \_ GETHELPTEXT** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4a968-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




