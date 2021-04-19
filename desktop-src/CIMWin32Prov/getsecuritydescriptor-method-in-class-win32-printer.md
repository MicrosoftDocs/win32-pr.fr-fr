---
description: Retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Méthode GetSecurityDescriptor de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514337"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="40a14-103">Méthode GetSecurityDescriptor de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="40a14-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="40a14-104">La méthode **GetSecurityDescriptor** retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="40a14-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="40a14-105">Le descripteur est retourné sous la forme d’une instance de l’expression [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="40a14-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="40a14-106">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="40a14-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="40a14-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="40a14-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40a14-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40a14-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40a14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40a14-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="40a14-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40a14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a14-111">*Descripteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="40a14-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40a14-112">Descripteur de sécurité associé à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="40a14-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a14-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40a14-113">Return value</span></span>

<span data-ttu-id="40a14-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="40a14-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="40a14-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="40a14-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="40a14-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="40a14-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="40a14-117">**0**</span><span class="sxs-lookup"><span data-stu-id="40a14-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="40a14-118">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="40a14-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="40a14-119">**2**</span><span class="sxs-lookup"><span data-stu-id="40a14-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="40a14-120">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="40a14-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="40a14-121">**8**</span><span class="sxs-lookup"><span data-stu-id="40a14-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="40a14-122">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="40a14-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="40a14-123">**9**</span><span class="sxs-lookup"><span data-stu-id="40a14-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="40a14-124">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="40a14-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="40a14-125">**21**</span><span class="sxs-lookup"><span data-stu-id="40a14-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="40a14-126">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="40a14-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40a14-127">Notes</span><span class="sxs-lookup"><span data-stu-id="40a14-127">Remarks</span></span>

<span data-ttu-id="40a14-128">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="40a14-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="40a14-129">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="40a14-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="40a14-130">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="40a14-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="40a14-131">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="40a14-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="40a14-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="40a14-132">Examples</span></span>

<span data-ttu-id="40a14-133">L’exemple de code VBScript suivant répertorie les imprimantes connectées à l’ordinateur local et obtient le descripteur de sécurité pour chaque imprimante.</span><span class="sxs-lookup"><span data-stu-id="40a14-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="40a14-134">Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de la liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) sont extraites pour déterminer les utilisateurs ayant accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="40a14-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="40a14-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40a14-135">Requirements</span></span>



| <span data-ttu-id="40a14-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40a14-136">Requirement</span></span> | <span data-ttu-id="40a14-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="40a14-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a14-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40a14-138">Minimum supported client</span></span><br/> | <span data-ttu-id="40a14-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40a14-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="40a14-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40a14-140">Minimum supported server</span></span><br/> | <span data-ttu-id="40a14-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40a14-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="40a14-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40a14-142">Namespace</span></span><br/>                | <span data-ttu-id="40a14-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="40a14-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="40a14-144">MOF</span><span class="sxs-lookup"><span data-stu-id="40a14-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40a14-145"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40a14-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="40a14-146">DLL</span><span class="sxs-lookup"><span data-stu-id="40a14-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40a14-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a14-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="40a14-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40a14-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a14-149">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="40a14-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="40a14-150">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="40a14-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="40a14-151">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="40a14-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="40a14-152">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="40a14-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

