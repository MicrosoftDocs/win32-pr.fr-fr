---
description: Obtient le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté. Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Obtient la méthode de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519937"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="616ae-105">Méthode d’obtient de la \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="616ae-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="616ae-106">La méthode **obtient** le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="616ae-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="616ae-107">Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="616ae-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="616ae-108">Si vous écrivez un script, utilisez la méthode [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="616ae-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="616ae-109">Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="616ae-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="616ae-110">L’utilisateur doit disposer de l’autorisation de **\_ contrôle de lecture** .</span><span class="sxs-lookup"><span data-stu-id="616ae-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="616ae-111">Par défaut, les administrateurs disposent de cette autorisation.</span><span class="sxs-lookup"><span data-stu-id="616ae-111">By default, administrators have that permission.</span></span> <span data-ttu-id="616ae-112">La seule partie du descripteur de sécurité qui est réellement utilisée est la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="616ae-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="616ae-113">La liste DACL peut contenir à la fois des ACE héritées et non héritées.</span><span class="sxs-lookup"><span data-stu-id="616ae-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="616ae-114">Les ACE Deny et allow sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="616ae-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="616ae-115">Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide de [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="616ae-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="616ae-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="616ae-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="616ae-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="616ae-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616ae-118">*SD* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="616ae-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="616ae-119">Descripteur de sécurité au format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="616ae-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616ae-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="616ae-120">Return value</span></span>

<span data-ttu-id="616ae-121">Cette méthode retourne un **HRESULT** indiquant l’état de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="616ae-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="616ae-122">La liste suivante répertorie les valeurs de retour dont l’importance **est déconseillée.**</span><span class="sxs-lookup"><span data-stu-id="616ae-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="616ae-123">Pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="616ae-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="616ae-124">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="616ae-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="616ae-125">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="616ae-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="616ae-126">Méthode exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="616ae-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="616ae-127">**\_accès WBEM \_ E \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="616ae-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="616ae-128">L’appelant ne dispose pas des droits suffisants pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="616ae-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="616ae-129">**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="616ae-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="616ae-130">Tentative d’exécution de cette méthode sur un système non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="616ae-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="616ae-131">Notes</span><span class="sxs-lookup"><span data-stu-id="616ae-131">Remarks</span></span>

<span data-ttu-id="616ae-132">Pour plus d’informations sur la modification de la sécurité des espaces de noms par programmation ou manuelle, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="616ae-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="616ae-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="616ae-133">Examples</span></span>

<span data-ttu-id="616ae-134">Le script suivant vous montre comment utiliser l'  objet pour obtenir le descripteur de sécurité actuel de l' \\ espace de noms Cimv2 racine et le remplacer par le tableau d’octets affiché dans la propriété distante.</span><span class="sxs-lookup"><span data-stu-id="616ae-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="616ae-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="616ae-135">Requirements</span></span>



| <span data-ttu-id="616ae-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="616ae-136">Requirement</span></span> | <span data-ttu-id="616ae-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="616ae-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="616ae-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="616ae-138">Minimum supported client</span></span><br/> | <span data-ttu-id="616ae-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="616ae-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="616ae-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="616ae-140">Minimum supported server</span></span><br/> | <span data-ttu-id="616ae-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="616ae-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="616ae-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="616ae-142">Namespace</span></span><br/>                | <span data-ttu-id="616ae-143">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="616ae-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="616ae-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="616ae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616ae-145">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="616ae-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="616ae-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="616ae-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="616ae-147">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="616ae-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="616ae-148">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="616ae-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="616ae-149">**\_\_SystemSecurity :: SetS**</span><span class="sxs-lookup"><span data-stu-id="616ae-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="616ae-150">**Descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="616ae-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="616ae-151">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="616ae-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="616ae-152">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="616ae-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

