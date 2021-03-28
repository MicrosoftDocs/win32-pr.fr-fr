---
description: Autorise le rappel à ajouter des éléments en haut du menu étendu.
title: Message DFM_MERGECONTEXTMENU_TOP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5810b5b6a0fc862b4dd8a9605cb9aa5c0c83afc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525354"
---
# <a name="dfm_mergecontextmenu_top-message"></a><span data-ttu-id="b73b4-103">\_Message DFM MERGECONTEXTMENU \_ Top</span><span class="sxs-lookup"><span data-stu-id="b73b4-103">DFM\_MERGECONTEXTMENU\_TOP message</span></span>

<span data-ttu-id="b73b4-104">Autorise le rappel à ajouter des éléments en haut du menu étendu.</span><span class="sxs-lookup"><span data-stu-id="b73b4-104">Allows the callback to add items to the top of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_TOP

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="b73b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b73b4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73b4-106">*pqcminfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b73b4-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73b4-107">Pointeur vers une structure [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenant les informations utilisées dans la fusion.</span><span class="sxs-lookup"><span data-stu-id="b73b4-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="b73b4-108">*uFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b73b4-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73b4-109">Indicateurs spécifiant comment le menu contextuel peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="b73b4-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="b73b4-110">Ce paramètre utilise les \_ \* valeurs CMF décrites dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b73b4-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b73b4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b73b4-111">Remarks</span></span>

<span data-ttu-id="b73b4-112">Si des éléments sont ajoutés au menu contextuel étendu, ils doivent être pris en charge avec les routines qui répondent de manière appropriée lorsque l’un de ces éléments est appelé à l’aide de [**DFM \_ commande InvokeCommand**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="b73b4-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="b73b4-113">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est implémenté.</span><span class="sxs-lookup"><span data-stu-id="b73b4-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="b73b4-114">Il existe deux API pour son implémentation, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b73b4-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="b73b4-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="b73b4-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b73b4-116">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="b73b4-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73b4-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b73b4-117">Requirements</span></span>



| <span data-ttu-id="b73b4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b73b4-118">Requirement</span></span> | <span data-ttu-id="b73b4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73b4-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b73b4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b73b4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b73b4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b73b4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b73b4-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b73b4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b73b4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b73b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b73b4-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b73b4-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




