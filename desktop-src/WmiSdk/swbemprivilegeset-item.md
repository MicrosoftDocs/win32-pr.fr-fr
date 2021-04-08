---
description: La méthode Item de l’objet SWbemPrivilegeSet retourne un objet SWbemPrivilege de la collection. La méthode Item est la méthode par défaut d’un objet SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: SWbemPrivilegeSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863766"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="a04b2-104">SWbemPrivilegeSet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="a04b2-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="a04b2-105">La méthode **Item** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) retourne un objet [**SWbemPrivilege**](swbemprivilege.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="a04b2-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="a04b2-106">La méthode **Item** est la méthode par défaut d’un objet **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="a04b2-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="a04b2-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a04b2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a04b2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a04b2-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="a04b2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a04b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04b2-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="a04b2-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="a04b2-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a04b2-111">Required.</span></span> <span data-ttu-id="a04b2-112">L’une des constantes WMI du groupe [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="a04b2-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="a04b2-113">Ces constantes sont essentiellement des entiers qui représentent des privilèges spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a04b2-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="a04b2-114">Par exemple, pour obtenir le privilège qui vous permet d’arrêter un système Windows, utilisez la constante **wbemPrivilegeShutdown** ou l’équivalent numérique 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="a04b2-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04b2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a04b2-115">Return value</span></span>

<span data-ttu-id="a04b2-116">En cas de réussite, l’objet [**SWbemPrivilege**](swbemprivilege.md) demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="a04b2-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a04b2-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a04b2-117">Error codes</span></span>

<span data-ttu-id="a04b2-118">À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a04b2-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a04b2-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a04b2-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a04b2-120">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a04b2-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a04b2-121">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="a04b2-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="a04b2-122">Le privilège spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a04b2-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a04b2-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="a04b2-123">Examples</span></span>

<span data-ttu-id="a04b2-124">L’exemple de code VBScript suivant utilise la méthode **Item**</span><span class="sxs-lookup"><span data-stu-id="a04b2-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="a04b2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a04b2-125">Requirements</span></span>



| <span data-ttu-id="a04b2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a04b2-126">Requirement</span></span> | <span data-ttu-id="a04b2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a04b2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a04b2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a04b2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a04b2-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a04b2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a04b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a04b2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a04b2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a04b2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a04b2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04b2-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04b2-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a04b2-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a04b2-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="a04b2-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a04b2-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a04b2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a04b2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04b2-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04b2-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a04b2-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="a04b2-138">CLSID</span></span><br/>                    | <span data-ttu-id="a04b2-139">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="a04b2-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="a04b2-140">IID</span><span class="sxs-lookup"><span data-stu-id="a04b2-140">IID</span></span><br/>                      | <span data-ttu-id="a04b2-141">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="a04b2-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="a04b2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a04b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04b2-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="a04b2-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="a04b2-144">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="a04b2-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="a04b2-145">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a04b2-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




