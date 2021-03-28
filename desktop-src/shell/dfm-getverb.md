---
description: Envoyé par l’implémentation du menu contextuel par défaut pour obtenir le verbe pour l’ID de commande donné dans le menu contextuel.
title: Message DFM_GETVERB (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201268"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="540f9-103">\_Message DFM GETVERB</span><span class="sxs-lookup"><span data-stu-id="540f9-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="540f9-104">Envoyé par l’implémentation du menu contextuel par défaut pour obtenir le verbe pour l’ID de commande donné dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="540f9-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="540f9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="540f9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="540f9-106">*idCmd \_ cchMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="540f9-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="540f9-107">Le mot de poids faible de ce paramètre contient l’ID de commande.</span><span class="sxs-lookup"><span data-stu-id="540f9-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="540f9-108">Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .</span><span class="sxs-lookup"><span data-stu-id="540f9-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="540f9-109">*pszText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="540f9-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="540f9-110">Pointeur vers une chaîne se terminant par un caractère null qui contient le texte de verbe.</span><span class="sxs-lookup"><span data-stu-id="540f9-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="540f9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="540f9-111">Remarks</span></span>

<span data-ttu-id="540f9-112">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit.</span><span class="sxs-lookup"><span data-stu-id="540f9-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="540f9-113">Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="540f9-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="540f9-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="540f9-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="540f9-115">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="540f9-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="540f9-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="540f9-116">Requirements</span></span>



| <span data-ttu-id="540f9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="540f9-117">Requirement</span></span> | <span data-ttu-id="540f9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="540f9-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="540f9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="540f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="540f9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="540f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="540f9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="540f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="540f9-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="540f9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="540f9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="540f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="540f9-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="540f9-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="540f9-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="540f9-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="540f9-126">**DFM \_ GETVERBW** (Unicode) et **DFM \_ GETVERBA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="540f9-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




