---
description: La méthode Add de l’objet SWbemPrivilegeSet ajoute un objet SWbemPrivilege à la collection SWbemPrivilegeSet. Si un privilège portant le même nom existe déjà dans la collection, il est remplacé.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Méthode SWbemPrivilegeSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034251"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="c5a93-104">SWbemPrivilegeSet. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="c5a93-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="c5a93-105">La méthode **Add** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="c5a93-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="c5a93-106">Si un privilège portant le même nom existe déjà dans la collection, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="c5a93-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="c5a93-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5a93-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a93-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5a93-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c5a93-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5a93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a93-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="c5a93-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a93-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c5a93-111">Required.</span></span> <span data-ttu-id="c5a93-112">L’une des constantes WMI du groupe [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="c5a93-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="c5a93-113">Ces constantes sont essentiellement des entiers qui représentent des privilèges spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c5a93-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="c5a93-114">Par exemple, pour ajouter le privilège qui vous permet d’arrêter un système informatique, utilisez la constante **wbemPrivilegeShutdown** .</span><span class="sxs-lookup"><span data-stu-id="c5a93-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="c5a93-115">Dans un script, vous devez utiliser l’équivalent numérique 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="c5a93-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="c5a93-116">Pour obtenir la liste complète de ces constantes et des chaînes de privilèges associées, consultez [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c5a93-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5a93-117">*bIsEnabled* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c5a93-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a93-118">Valeur booléenne qui active ou désactive ce privilège.</span><span class="sxs-lookup"><span data-stu-id="c5a93-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="c5a93-119">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="c5a93-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a93-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5a93-120">Return value</span></span>

<span data-ttu-id="c5a93-121">En cas de réussite, la méthode retourne un objet [**SWbemPrivilege**](swbemprivilege.md) qui représente le nouveau privilège.</span><span class="sxs-lookup"><span data-stu-id="c5a93-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="c5a93-122">Dans le cas contraire, un objet null est retourné.</span><span class="sxs-lookup"><span data-stu-id="c5a93-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5a93-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c5a93-123">Error codes</span></span>

<span data-ttu-id="c5a93-124">À la fin de la méthode **Add** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="c5a93-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c5a93-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c5a93-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c5a93-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c5a93-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c5a93-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="c5a93-127">Examples</span></span>

<span data-ttu-id="c5a93-128">Un exemple de code utilisant cette méthode est décrit dans la rubrique [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a93-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a93-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5a93-129">Requirements</span></span>



| <span data-ttu-id="c5a93-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5a93-130">Requirement</span></span> | <span data-ttu-id="c5a93-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5a93-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a93-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5a93-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a93-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5a93-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5a93-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5a93-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a93-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5a93-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5a93-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5a93-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a93-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a93-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5a93-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c5a93-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5a93-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5a93-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5a93-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c5a93-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5a93-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5a93-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5a93-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5a93-142">CLSID</span></span><br/>                    | <span data-ttu-id="c5a93-143">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="c5a93-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="c5a93-144">IID</span><span class="sxs-lookup"><span data-stu-id="c5a93-144">IID</span></span><br/>                      | <span data-ttu-id="c5a93-145">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="c5a93-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c5a93-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5a93-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a93-147">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="c5a93-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="c5a93-148">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="c5a93-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="c5a93-149">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="c5a93-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="c5a93-150">**SWbemPrivilegeSet.AddAsString**</span><span class="sxs-lookup"><span data-stu-id="c5a93-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="c5a93-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="c5a93-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="c5a93-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="c5a93-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="c5a93-153">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="c5a93-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




