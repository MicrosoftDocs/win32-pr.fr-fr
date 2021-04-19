---
description: Vous pouvez utiliser la méthode AddAsString de l’objet SWbemPrivilegeSet pour ajouter un privilège à une collection SWbemPrivilegeSet à l’aide d’une chaîne de privilèges.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Méthode SWbemPrivilegeSet. AddAsString (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543745"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="7f968-103">Méthode SWbemPrivilegeSet. AddAsString</span><span class="sxs-lookup"><span data-stu-id="7f968-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="7f968-104">Vous pouvez utiliser la méthode **AddAsString** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) pour ajouter un privilège à une collection **SWbemPrivilegeSet** à l’aide d’une chaîne de privilèges.</span><span class="sxs-lookup"><span data-stu-id="7f968-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="7f968-105">Utilisez cette méthode pour ajouter un privilège ou pour activer un privilège pour les objets [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="7f968-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="7f968-106">Consultez [exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7f968-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="7f968-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7f968-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f968-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f968-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7f968-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f968-110">*strPrivilege*</span><span class="sxs-lookup"><span data-stu-id="7f968-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="7f968-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7f968-111">Required.</span></span> <span data-ttu-id="7f968-112">Une des chaînes de privilège.</span><span class="sxs-lookup"><span data-stu-id="7f968-112">One of the privilege strings.</span></span> <span data-ttu-id="7f968-113">Pour obtenir la liste complète de ces chaînes et des constantes WMI associées, consultez [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7f968-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="7f968-114">Chaque chaîne de privilège représente un privilège spécifique.</span><span class="sxs-lookup"><span data-stu-id="7f968-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="7f968-115">Par exemple, pour ajouter le privilège qui utilise pour arrêter un système informatique, utilisez la chaîne **SeShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="7f968-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="7f968-116">*bIsEnabled* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7f968-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f968-117">Valeur booléenne qui active ou désactive ce privilège.</span><span class="sxs-lookup"><span data-stu-id="7f968-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="7f968-118">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="7f968-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f968-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f968-119">Return value</span></span>

<span data-ttu-id="7f968-120">En cas de réussite, cette méthode retourne un objet [**SWbemPrivilege**](swbemprivilege.md) qui représente le nouveau privilège.</span><span class="sxs-lookup"><span data-stu-id="7f968-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="7f968-121">Dans le cas contraire, un objet null est retourné.</span><span class="sxs-lookup"><span data-stu-id="7f968-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f968-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7f968-122">Error codes</span></span>

<span data-ttu-id="7f968-123">À la fin de la méthode **AddAsString** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="7f968-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7f968-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7f968-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7f968-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7f968-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7f968-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="7f968-126">Examples</span></span>

<span data-ttu-id="7f968-127">L’exemple de code VBScript suivant crée un nouveau port pour un serveur d’impression à l’aide de [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span><span class="sxs-lookup"><span data-stu-id="7f968-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="7f968-128">**SeLoadDriverPrivilege** est requis pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7f968-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="7f968-129">Consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7f968-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="7f968-130">Un exemple de code qui utilise cette méthode est également décrit dans la rubrique [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="7f968-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f968-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f968-131">Requirements</span></span>



| <span data-ttu-id="7f968-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f968-132">Requirement</span></span> | <span data-ttu-id="7f968-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f968-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f968-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f968-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7f968-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f968-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f968-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f968-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7f968-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f968-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f968-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f968-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f968-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f968-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f968-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7f968-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f968-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f968-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f968-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7f968-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f968-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f968-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f968-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="7f968-144">CLSID</span></span><br/>                    | <span data-ttu-id="7f968-145">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="7f968-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="7f968-146">IID</span><span class="sxs-lookup"><span data-stu-id="7f968-146">IID</span></span><br/>                      | <span data-ttu-id="7f968-147">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="7f968-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="7f968-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f968-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f968-149">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="7f968-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="7f968-150">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="7f968-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="7f968-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="7f968-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="7f968-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="7f968-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="7f968-153">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="7f968-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="7f968-154">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="7f968-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="7f968-155">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7f968-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

