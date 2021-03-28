---
description: Envoyé pour vérifier l’existence d’une commande de menu.
title: Message DFM_VALIDATECMD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112338"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="ff1ad-103">\_Message DFM VALIDATECMD</span><span class="sxs-lookup"><span data-stu-id="ff1ad-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="ff1ad-104">Envoyé pour vérifier l’existence d’une commande de menu.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="ff1ad-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff1ad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1ad-106">*idCmd*</span><span class="sxs-lookup"><span data-stu-id="ff1ad-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="ff1ad-107">Décalage de l’identificateur de la commande de menu.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="ff1ad-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff1ad-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ff1ad-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-109">Not used.</span></span> <span data-ttu-id="ff1ad-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1ad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff1ad-111">Return value</span></span>

<span data-ttu-id="ff1ad-112">Retourne S \_ OK si la commande existe, ou a la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1ad-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ff1ad-113">Remarks</span></span>

<span data-ttu-id="ff1ad-114">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="ff1ad-115">Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="ff1ad-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="ff1ad-116">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="ff1ad-117">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="ff1ad-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1ad-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff1ad-118">Requirements</span></span>



| <span data-ttu-id="ff1ad-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff1ad-119">Requirement</span></span> | <span data-ttu-id="ff1ad-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff1ad-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1ad-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff1ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1ad-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff1ad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ff1ad-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff1ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1ad-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff1ad-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ff1ad-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff1ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1ad-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ad-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




