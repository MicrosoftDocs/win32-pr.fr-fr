---
description: Envoyé par l’implémentation du menu contextuel par défaut pour demander la fonction de rappel qui gère le menu (LPFNDFMCALLBACK) pour appeler une commande de menu.
title: Message DFM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972018"
---
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="9b6e7-103">\_Message DFM commande InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="9b6e7-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="9b6e7-104">Envoyé par l’implémentation du menu contextuel par défaut pour demander la fonction de rappel qui gère le menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) pour appeler une commande de menu.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="9b6e7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b6e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6e7-106">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6e7-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6e7-107">ID de commande de la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="9b6e7-108">Les indicateurs suivants sont reconnus :</span><span class="sxs-lookup"><span data-stu-id="9b6e7-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="9b6e7-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-110">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-110">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-111">Supprimer l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="9b6e7-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ cmd \_ Move**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-113">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-113">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-114">Déplacer l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="9b6e7-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copie cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-116">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-116">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-117">Copier l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="9b6e7-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_lien cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-119">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-119">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-120">Créer un lien vers l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="9b6e7-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Propriétés de cmd DFM \_**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-122">Affichez l’interface utilisateur des **Propriétés** de l’élément sur lequel le menu a été appelé.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="9b6e7-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="9b6e7-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd \_ coller**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-126">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-126">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-127">Collez un élément à l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="9b6e7-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ VIEWLIST**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-129">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="9b6e7-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-131">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="9b6e7-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-133">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-133">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-134">Collez un lien à l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="9b6e7-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-136">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="9b6e7-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-138">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="9b6e7-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ cmd \_ Renommer**</span><span class="sxs-lookup"><span data-stu-id="9b6e7-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="9b6e7-140">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-140">**Windows Vista and later**.</span></span> <span data-ttu-id="9b6e7-141">Renommez l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b6e7-142">*arguments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b6e7-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6e7-143">Pointeur vers une chaîne se terminant par un caractère null qui contient des arguments supplémentaires pour la commande de menu sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="9b6e7-144">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6e7-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b6e7-145">Return value</span></span>

<span data-ttu-id="9b6e7-146">Le gestionnaire de ce message doit retourner la \_ valeur false si vous souhaitez que l’implémentation par défaut appelle le gestionnaire par défaut pour la commande.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="9b6e7-147">Retourne S \_ OK si le message a été géré.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="9b6e7-148">Sinon, retourne un code d’erreur HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b6e7-149">Notes</span><span class="sxs-lookup"><span data-stu-id="9b6e7-149">Remarks</span></span>

<span data-ttu-id="9b6e7-150">Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont le rappel est implémenté.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="9b6e7-151">Il existe deux API pour la construction de rappel, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) qui prend un pointeur vers une fonction de rappel, ou [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) qui utilise un objet de rappel qui prend en charge [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="9b6e7-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="9b6e7-152">Les éléments sur lesquels la commande est appelée sont fournis dans un objet de données passé à la fonction de rappel ou à la méthode [**IContextMenuCB :: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="9b6e7-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="9b6e7-153">Cet objet de données est fourni par la source de données qui implémente le rappel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="9b6e7-154">Pour extraire les éléments de l’objet de données, utilisez [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="9b6e7-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="9b6e7-155">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="9b6e7-156">Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6e7-157">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b6e7-157">Requirements</span></span>



| <span data-ttu-id="9b6e7-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b6e7-158">Requirement</span></span> | <span data-ttu-id="9b6e7-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b6e7-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6e7-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6e7-160">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6e7-161">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b6e7-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b6e7-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6e7-162">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6e7-163">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b6e7-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b6e7-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b6e7-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b6e7-165"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b6e7-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
