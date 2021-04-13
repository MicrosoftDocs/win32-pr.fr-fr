---
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201136"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="af0bc-103">Méthode SetSecurityDescriptor de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="af0bc-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="af0bc-104">La méthode **SetSecurityDescriptor** écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="af0bc-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="af0bc-105">Le descripteur de sécurité est une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="af0bc-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="af0bc-106">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="af0bc-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="af0bc-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="af0bc-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="af0bc-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="af0bc-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="af0bc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af0bc-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="af0bc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af0bc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af0bc-111">*Descripteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af0bc-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-112">Descripteur de sécurité associé à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="af0bc-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af0bc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af0bc-113">Return value</span></span>

<span data-ttu-id="af0bc-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="af0bc-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="af0bc-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="af0bc-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="af0bc-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="af0bc-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="af0bc-117">**0**</span><span class="sxs-lookup"><span data-stu-id="af0bc-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-118">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="af0bc-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="af0bc-119">**2**</span><span class="sxs-lookup"><span data-stu-id="af0bc-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-120">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="af0bc-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="af0bc-121">**8**</span><span class="sxs-lookup"><span data-stu-id="af0bc-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-122">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="af0bc-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="af0bc-123">**9**</span><span class="sxs-lookup"><span data-stu-id="af0bc-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-124">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="af0bc-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="af0bc-125">**21**</span><span class="sxs-lookup"><span data-stu-id="af0bc-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="af0bc-126">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="af0bc-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af0bc-127">Notes</span><span class="sxs-lookup"><span data-stu-id="af0bc-127">Remarks</span></span>

<span data-ttu-id="af0bc-128">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="af0bc-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="af0bc-129">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="af0bc-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="af0bc-130">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="af0bc-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="af0bc-131">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="af0bc-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="af0bc-132">Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="af0bc-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="af0bc-133">Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="af0bc-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="af0bc-134">**SE \_ DACL en \_ présence**</span><span class="sxs-lookup"><span data-stu-id="af0bc-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="af0bc-135">Indique que la liste DACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="af0bc-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="af0bc-136">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="af0bc-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="af0bc-137">**\_liste SACL se \_ présente**</span><span class="sxs-lookup"><span data-stu-id="af0bc-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="af0bc-138">Indique que la liste SACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="af0bc-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="af0bc-139">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="af0bc-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="af0bc-140">Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte.</span><span class="sxs-lookup"><span data-stu-id="af0bc-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="af0bc-141">Pour les scripts, le nom du privilège est **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="af0bc-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="af0bc-142">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="af0bc-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="af0bc-143">Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="af0bc-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="af0bc-144">Dans le cas contraire, WMI conserve les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="af0bc-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="af0bc-145">Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="af0bc-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="af0bc-146">Quand une nouvelle SACL est **null** dans un appel à cette méthode, alors le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="af0bc-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="af0bc-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="af0bc-147">Examples</span></span>

<span data-ttu-id="af0bc-148">L’exemple PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) remplace les autorisations (ACL) d’une imprimante à une autre.</span><span class="sxs-lookup"><span data-stu-id="af0bc-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="af0bc-149">L’exemple de code PowerShell suivant décrit comment définir le descripteur de sécurité d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="af0bc-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="af0bc-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af0bc-150">Requirements</span></span>



| <span data-ttu-id="af0bc-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af0bc-151">Requirement</span></span> | <span data-ttu-id="af0bc-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="af0bc-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="af0bc-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af0bc-153">Minimum supported client</span></span><br/> | <span data-ttu-id="af0bc-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af0bc-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="af0bc-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af0bc-155">Minimum supported server</span></span><br/> | <span data-ttu-id="af0bc-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af0bc-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="af0bc-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af0bc-157">Namespace</span></span><br/>                | <span data-ttu-id="af0bc-158">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="af0bc-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="af0bc-159">MOF</span><span class="sxs-lookup"><span data-stu-id="af0bc-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af0bc-160"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af0bc-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="af0bc-161">DLL</span><span class="sxs-lookup"><span data-stu-id="af0bc-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af0bc-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af0bc-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="af0bc-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af0bc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0bc-164">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="af0bc-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="af0bc-165">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="af0bc-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="af0bc-166">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="af0bc-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="af0bc-167">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="af0bc-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

