---
description: Autorise le rappel à ajouter des éléments au menu.
title: Message DFM_MERGECONTEXTMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972010"
---
# <a name="dfm_mergecontextmenu-message"></a><span data-ttu-id="b4783-103">\_Message DFM MERGECONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="b4783-103">DFM\_MERGECONTEXTMENU message</span></span>

<span data-ttu-id="b4783-104">Autorise le rappel à ajouter des éléments au menu.</span><span class="sxs-lookup"><span data-stu-id="b4783-104">Allows the callback to add items to the menu.</span></span>


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="b4783-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4783-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4783-106">*pqcminfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4783-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4783-107">Pointeur vers une structure [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenant les informations utilisées dans la fusion.</span><span class="sxs-lookup"><span data-stu-id="b4783-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="b4783-108">*uFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4783-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4783-109">Indicateurs spécifiant comment le menu contextuel peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="b4783-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="b4783-110">Ce paramètre utilise les \_ \* valeurs CMF décrites dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b4783-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4783-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b4783-111">Remarks</span></span>

<span data-ttu-id="b4783-112">Si des éléments sont ajoutés au menu contextuel, ils doivent être pris en charge avec les routines qui répondent de manière appropriée lorsque l’un de ces éléments est appelé à l’aide de [**DFM \_ commande InvokeCommand**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="b4783-112">If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="b4783-113">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est implémenté.</span><span class="sxs-lookup"><span data-stu-id="b4783-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="b4783-114">Il existe deux API pour son implémentation, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b4783-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="b4783-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="b4783-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b4783-116">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="b4783-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4783-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b4783-117">Requirements</span></span>



| <span data-ttu-id="b4783-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4783-118">Requirement</span></span> | <span data-ttu-id="b4783-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4783-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4783-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4783-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4783-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4783-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b4783-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4783-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4783-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4783-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4783-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4783-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4783-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4783-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




