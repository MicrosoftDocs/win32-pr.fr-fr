---
description: Obtient le descripteur de sécurité qui contrôle les personnes autorisées à démarrer une application DCOM.
ms.assetid: ba02807f-aa2a-4b1c-9692-2803d93cd2ee
ms.tgt_platform: multiple
title: Méthode GetLaunchSecurityDescriptor de la classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6d434c0cc9a4d236350f3dd4d15cf9d8c8e5ad4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200951"
---
# <a name="getlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="49a51-103">Méthode GetLaunchSecurityDescriptor de la \_ classe Win32 DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="49a51-103">GetLaunchSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="49a51-104">La méthode WMI **GetLaunchSecurityDescriptor** obtient le descripteur de sécurité qui contrôle les personnes autorisées à démarrer une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="49a51-104">The **GetLaunchSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to start a DCOM application.</span></span> <span data-ttu-id="49a51-105">Le descripteur de sécurité est une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="49a51-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="49a51-106">Le compte qui exécute le script ou l’application qui appelle cette méthode doit avoir les privilèges **SeSecurityPrivilege** et **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="49a51-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="49a51-107">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="49a51-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="49a51-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49a51-108">Syntax</span></span>


```mof
uint32 GetLaunchSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="49a51-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49a51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a51-110">*Descripteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49a51-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49a51-111">Descripteur de sécurité permettant de définir les personnes qui peuvent démarrer l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="49a51-111">The security descriptor to set that controls who can start the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a51-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49a51-112">Return value</span></span>

<span data-ttu-id="49a51-113">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="49a51-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="49a51-114">Pour plus d’informations, consultez [codes de retour WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="49a51-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="49a51-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="49a51-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-116">0</span><span class="sxs-lookup"><span data-stu-id="49a51-116">0</span></span>

<span data-ttu-id="49a51-117">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="49a51-117">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="49a51-118">**2**</span><span class="sxs-lookup"><span data-stu-id="49a51-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-119">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="49a51-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="49a51-120">**8**</span><span class="sxs-lookup"><span data-stu-id="49a51-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-121">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="49a51-121">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="49a51-122">**9**</span><span class="sxs-lookup"><span data-stu-id="49a51-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-123">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="49a51-123">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="49a51-124">**21**</span><span class="sxs-lookup"><span data-stu-id="49a51-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-125">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="49a51-125">A parameter specified in the method call is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49a51-126">**Autres**</span><span class="sxs-lookup"><span data-stu-id="49a51-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="49a51-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="49a51-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49a51-128">Notes</span><span class="sxs-lookup"><span data-stu-id="49a51-128">Remarks</span></span>

<span data-ttu-id="49a51-129">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="49a51-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="49a51-130">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="49a51-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="49a51-131">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="49a51-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="49a51-132">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="49a51-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="49a51-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49a51-133">Requirements</span></span>



| <span data-ttu-id="49a51-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49a51-134">Requirement</span></span> | <span data-ttu-id="49a51-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="49a51-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49a51-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a51-136">Minimum supported client</span></span><br/> | <span data-ttu-id="49a51-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49a51-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49a51-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a51-138">Minimum supported server</span></span><br/> | <span data-ttu-id="49a51-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49a51-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49a51-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49a51-140">Namespace</span></span><br/>                | <span data-ttu-id="49a51-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="49a51-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49a51-142">MOF</span><span class="sxs-lookup"><span data-stu-id="49a51-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49a51-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49a51-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49a51-144">DLL</span><span class="sxs-lookup"><span data-stu-id="49a51-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49a51-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49a51-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a51-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49a51-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a51-147">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="49a51-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="49a51-148">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="49a51-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="49a51-149">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="49a51-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="49a51-150">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="49a51-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

