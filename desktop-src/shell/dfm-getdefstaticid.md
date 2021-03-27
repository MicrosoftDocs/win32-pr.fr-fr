---
description: Envoyé par l’implémentation du menu contextuel par défaut lors de la création, en spécifiant la commande de menu par défaut et en autorisant l’autre choix à effectuer. Utilisé par LPFNDFMCALLBACK.
title: Message DFM_GETDEFSTATICID (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393440"
---
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="305bc-104">\_Message DFM GETDEFSTATICID</span><span class="sxs-lookup"><span data-stu-id="305bc-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="305bc-105">Envoyé par l’implémentation du menu contextuel par défaut lors de la création, en spécifiant la commande de menu par défaut et en autorisant l’autre choix à effectuer.</span><span class="sxs-lookup"><span data-stu-id="305bc-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="305bc-106">Utilisé par [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span><span class="sxs-lookup"><span data-stu-id="305bc-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="305bc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="305bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="305bc-108">*defaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="305bc-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="305bc-109">Pointeur vers l’ID de la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="305bc-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="305bc-110">L’indicateur suivant est reconnu.</span><span class="sxs-lookup"><span data-stu-id="305bc-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="305bc-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Propriétés de cmd DFM \_**</span><span class="sxs-lookup"><span data-stu-id="305bc-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="305bc-112">Affichez l’interface utilisateur des **Propriétés** de l’élément sur lequel le menu a été appelé.</span><span class="sxs-lookup"><span data-stu-id="305bc-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="305bc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="305bc-113">Remarks</span></span>

<span data-ttu-id="305bc-114">Pour remplacer le choix de commande par défaut, votre gestionnaire doit, lors de la réception de ce message, définir la valeur pointée par *defaultID* sur l’ID de la commande de remplacement et retourner \_ OK.</span><span class="sxs-lookup"><span data-stu-id="305bc-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="305bc-115">Sinon, retourne un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="305bc-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="305bc-116">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit.</span><span class="sxs-lookup"><span data-stu-id="305bc-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="305bc-117">Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="305bc-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="305bc-118">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="305bc-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="305bc-119">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="305bc-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="305bc-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="305bc-120">Requirements</span></span>



| <span data-ttu-id="305bc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="305bc-121">Requirement</span></span> | <span data-ttu-id="305bc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="305bc-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="305bc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="305bc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="305bc-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="305bc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="305bc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="305bc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="305bc-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="305bc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="305bc-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="305bc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="305bc-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="305bc-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
