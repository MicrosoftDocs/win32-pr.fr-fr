---
description: Envoyé par l’implémentation du menu contextuel par défaut pour assigner un nom à une commande de menu.
title: Message DFM_MAPCOMMANDNAME (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525359"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="d5f21-103">\_Message DFM MAPCOMMANDNAME</span><span class="sxs-lookup"><span data-stu-id="d5f21-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="d5f21-104">Envoyé par l’implémentation du menu contextuel par défaut pour assigner un nom à une commande de menu.</span><span class="sxs-lookup"><span data-stu-id="d5f21-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="d5f21-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5f21-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f21-106">*defaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5f21-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f21-107">Pointeur vers l’ID de la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d5f21-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="d5f21-108">*pszCommandName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5f21-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f21-109">Pointeur vers une chaîne Unicode contenant le nom de la commande.</span><span class="sxs-lookup"><span data-stu-id="d5f21-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5f21-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d5f21-110">Remarks</span></span>

<span data-ttu-id="d5f21-111">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est implémenté.</span><span class="sxs-lookup"><span data-stu-id="d5f21-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="d5f21-112">Il existe deux API pour son implémentation, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="d5f21-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="d5f21-113">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="d5f21-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="d5f21-114">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="d5f21-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f21-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d5f21-115">Requirements</span></span>



| <span data-ttu-id="d5f21-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5f21-116">Requirement</span></span> | <span data-ttu-id="d5f21-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5f21-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f21-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f21-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f21-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d5f21-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f21-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f21-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d5f21-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5f21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f21-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f21-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




