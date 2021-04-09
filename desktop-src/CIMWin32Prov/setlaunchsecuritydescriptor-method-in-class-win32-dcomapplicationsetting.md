---
description: Met à jour le descripteur de sécurité de lancement de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance d’une \_ classe Win32 SecurityDescriptor.
ms.assetid: 72245d22-1a0a-4069-b5d6-9d59e4de4aab
ms.tgt_platform: multiple
title: Méthode SetLaunchSecurityDescriptor de la classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a99919246d7b36aa265d36ae0f75e8347ea6a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861313"
---
# <a name="setlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="7610d-103">Méthode SetLaunchSecurityDescriptor de la \_ classe Win32 DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="7610d-103">SetLaunchSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="7610d-104">La méthode **SetLaunchSecurityDescriptor** met à jour le descripteur de sécurité de lancement de l’application DCOM avec un nouveau descripteur de sécurité qui est défini par une instance d’une classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7610d-104">The **SetLaunchSecurityDescriptor** method updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="7610d-105">Ce descripteur de sécurité détermine qui est autorisé à lancer l’application.</span><span class="sxs-lookup"><span data-stu-id="7610d-105">This security descriptor controls who is allowed to launch the application.</span></span> <span data-ttu-id="7610d-106">Le compte qui exécute le script ou l’application qui appelle cette méthode doit avoir les privilèges **SeSecurityPrivilege** et **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="7610d-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="7610d-107">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="7610d-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="7610d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7610d-108">Syntax</span></span>


```mof
uint32 SetLaunchSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="7610d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7610d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7610d-110">*Descripteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7610d-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7610d-111">Descripteur de sécurité permettant de définir les personnes qui peuvent démarrer l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="7610d-111">The security descriptor to set that controls who can start the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7610d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7610d-112">Return value</span></span>

<span data-ttu-id="7610d-113">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7610d-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="7610d-114">Pour plus d’informations, consultez [codes de retour WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7610d-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="7610d-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="7610d-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-116">0</span><span class="sxs-lookup"><span data-stu-id="7610d-116">0</span></span>

<span data-ttu-id="7610d-117">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="7610d-117">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="7610d-118">**2**</span><span class="sxs-lookup"><span data-stu-id="7610d-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-119">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="7610d-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7610d-120">**8**</span><span class="sxs-lookup"><span data-stu-id="7610d-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-121">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="7610d-121">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7610d-122">**9**</span><span class="sxs-lookup"><span data-stu-id="7610d-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-123">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="7610d-123">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="7610d-124">**21**</span><span class="sxs-lookup"><span data-stu-id="7610d-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-125">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7610d-125">A parameter specified in the method call is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7610d-126">**Autres**</span><span class="sxs-lookup"><span data-stu-id="7610d-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7610d-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="7610d-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7610d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7610d-128">Remarks</span></span>

<span data-ttu-id="7610d-129">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="7610d-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="7610d-130">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="7610d-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="7610d-131">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="7610d-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="7610d-132">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="7610d-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="7610d-133">Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="7610d-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="7610d-134">Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7610d-134">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="7610d-135">**SE \_ DACL en \_ présence**</span><span class="sxs-lookup"><span data-stu-id="7610d-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="7610d-136">Indique que la liste DACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7610d-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="7610d-137">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="7610d-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="7610d-138">**\_liste SACL se \_ présente**</span><span class="sxs-lookup"><span data-stu-id="7610d-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="7610d-139">Indique que la liste SACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7610d-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="7610d-140">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="7610d-140">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="7610d-141">Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte.</span><span class="sxs-lookup"><span data-stu-id="7610d-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="7610d-142">Pour les scripts, le nom du privilège est **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="7610d-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="7610d-143">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="7610d-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="7610d-144">Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7610d-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="7610d-145">Dans le cas contraire, WMI conserve les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="7610d-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="7610d-146">Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="7610d-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="7610d-147">Quand une nouvelle SACL est **null** dans un appel à cette méthode, alors le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="7610d-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="7610d-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7610d-148">Requirements</span></span>



| <span data-ttu-id="7610d-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7610d-149">Requirement</span></span> | <span data-ttu-id="7610d-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="7610d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7610d-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7610d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7610d-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7610d-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7610d-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7610d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7610d-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7610d-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7610d-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7610d-155">Namespace</span></span><br/>                | <span data-ttu-id="7610d-156">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7610d-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7610d-157">MOF</span><span class="sxs-lookup"><span data-stu-id="7610d-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7610d-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7610d-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7610d-159">DLL</span><span class="sxs-lookup"><span data-stu-id="7610d-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7610d-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7610d-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7610d-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7610d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7610d-162">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="7610d-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="7610d-163">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="7610d-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="7610d-164">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="7610d-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="7610d-165">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="7610d-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

