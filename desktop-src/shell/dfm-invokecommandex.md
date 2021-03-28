---
description: Envoyé par l’implémentation du menu contextuel par défaut pour demander à LPFNDFMCALLBACK d’appeler une commande de menu étendue.
title: Message DFM_INVOKECOMMANDEX (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525360"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="173da-103">\_Message DFM INVOKECOMMANDEX</span><span class="sxs-lookup"><span data-stu-id="173da-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="173da-104">Envoyé par l’implémentation du menu contextuel par défaut pour demander à [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) d’appeler une commande de menu étendue.</span><span class="sxs-lookup"><span data-stu-id="173da-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="173da-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="173da-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="173da-106">*idCmd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="173da-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="173da-107">ID de commande de la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="173da-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="173da-108">Les indicateurs suivants sont reconnus.</span><span class="sxs-lookup"><span data-stu-id="173da-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="173da-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="173da-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="173da-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ cmd \_ Move**</span><span class="sxs-lookup"><span data-stu-id="173da-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="173da-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copie cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="173da-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="173da-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_lien cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="173da-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="173da-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Propriétés de cmd DFM \_**</span><span class="sxs-lookup"><span data-stu-id="173da-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="173da-114">Affichez l’interface utilisateur des **Propriétés** de l’élément sur lequel le menu a été appelé.</span><span class="sxs-lookup"><span data-stu-id="173da-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="173da-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="173da-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="173da-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd \_ coller**</span><span class="sxs-lookup"><span data-stu-id="173da-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="173da-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="173da-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="173da-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="173da-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="173da-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="173da-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="173da-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="173da-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="173da-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="173da-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="173da-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ cmd \_ Renommer**</span><span class="sxs-lookup"><span data-stu-id="173da-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="173da-123">*PDFMICS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="173da-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="173da-124">Pointeur vers une structure [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) qui contient des arguments supplémentaires pour la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="173da-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="173da-125">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="173da-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="173da-126">Notes</span><span class="sxs-lookup"><span data-stu-id="173da-126">Remarks</span></span>

<span data-ttu-id="173da-127">À la réception de ce message, votre fonction doit retourner S \_ false si vous souhaitez que l’implémentation par défaut appelle le gestionnaire par défaut pour la commande.</span><span class="sxs-lookup"><span data-stu-id="173da-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="173da-128">Retourne S \_ OK si le message a été géré.</span><span class="sxs-lookup"><span data-stu-id="173da-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="173da-129">Sinon, retourne un code d’erreur HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="173da-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="173da-130">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont le rappel est implémenté.</span><span class="sxs-lookup"><span data-stu-id="173da-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="173da-131">Il existe deux API pour la construction de rappel, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) qui prend un pointeur vers une fonction de rappel, ou [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) qui utilise un objet de rappel qui prend en charge [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="173da-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="173da-132">Les éléments sur lesquels la commande est appelée sont fournis dans un objet de données passé à la fonction de rappel ou à la méthode [**IContextMenuCB :: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="173da-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="173da-133">Cet objet de données est fourni par la source de données qui implémente le rappel.</span><span class="sxs-lookup"><span data-stu-id="173da-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="173da-134">Pour extraire les éléments de l’objet de données, utilisez [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="173da-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="173da-135">[**DFM \_ COMMANDE INVOKECOMMAND**](dfm-invokecommand.md) est une version plus simple de ce message qui ne fournit pas autant d’informations que le rappel.</span><span class="sxs-lookup"><span data-stu-id="173da-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="173da-136">Utilisez **DFM \_ commande InvokeCommand** si les informations supplémentaires fournies par **DFM \_ INVOKECOMMANDEX** ne sont pas nécessaires dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="173da-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="173da-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="173da-137">Requirements</span></span>



| <span data-ttu-id="173da-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="173da-138">Requirement</span></span> | <span data-ttu-id="173da-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="173da-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="173da-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="173da-140">Minimum supported client</span></span><br/> | <span data-ttu-id="173da-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="173da-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="173da-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="173da-142">Minimum supported server</span></span><br/> | <span data-ttu-id="173da-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="173da-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="173da-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="173da-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="173da-145"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="173da-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
