---
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté. Le descripteur de sécurité est représenté par une instance de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541856"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="de1a9-104">Méthode SetSecurityDescriptor de la \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="de1a9-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="de1a9-105">La méthode [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="de1a9-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="de1a9-106">Le descripteur de sécurité est représenté par une instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="de1a9-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="de1a9-107">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="de1a9-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="de1a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de1a9-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="de1a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de1a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1a9-110">*Descripteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de1a9-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-111">Descripteur de sécurité associé à l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="de1a9-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1a9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de1a9-112">Return value</span></span>

<span data-ttu-id="de1a9-113">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="de1a9-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="de1a9-114">Pour plus d’informations, consultez [codes de retour WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="de1a9-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="de1a9-115">**0**</span><span class="sxs-lookup"><span data-stu-id="de1a9-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-116">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="de1a9-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="de1a9-117">**2**</span><span class="sxs-lookup"><span data-stu-id="de1a9-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-118">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="de1a9-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="de1a9-119">**8**</span><span class="sxs-lookup"><span data-stu-id="de1a9-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-120">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="de1a9-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="de1a9-121">**9**</span><span class="sxs-lookup"><span data-stu-id="de1a9-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-122">L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="de1a9-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="de1a9-123">**21**</span><span class="sxs-lookup"><span data-stu-id="de1a9-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="de1a9-124">Un paramètre spécifié dans l’appel de méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="de1a9-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de1a9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="de1a9-125">Remarks</span></span>

<span data-ttu-id="de1a9-126">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de Access Control système*](/windows/desktop/SecGloss/a-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="de1a9-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="de1a9-127">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="de1a9-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="de1a9-128">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="de1a9-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="de1a9-129">Pour plus d’informations, consultez [**constantes de privilège**](privilege-constants.md) et [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="de1a9-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="de1a9-130">Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="de1a9-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="de1a9-131">Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL ou la liste SACL ou les deux sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="de1a9-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="de1a9-132">**SE \_ DACL en \_ présence**</span><span class="sxs-lookup"><span data-stu-id="de1a9-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="de1a9-133">Indique que la liste DACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="de1a9-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="de1a9-134">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="de1a9-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="de1a9-135">**\_liste SACL se \_ présente**</span><span class="sxs-lookup"><span data-stu-id="de1a9-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="de1a9-136">Indique que la liste SACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="de1a9-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="de1a9-137">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="de1a9-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="de1a9-138">Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte.</span><span class="sxs-lookup"><span data-stu-id="de1a9-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="de1a9-139">Pour les scripts, le nom du privilège est **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="de1a9-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="de1a9-140">Pour plus d’informations, consultez [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="de1a9-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="de1a9-141">Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="de1a9-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="de1a9-142">Dans le cas contraire, WMI conserve les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="de1a9-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="de1a9-143">Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="de1a9-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="de1a9-144">Quand une nouvelle SACL a la **valeur null** dans un appel de cette méthode, le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="de1a9-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1a9-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de1a9-145">Requirements</span></span>



| <span data-ttu-id="de1a9-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de1a9-146">Requirement</span></span> | <span data-ttu-id="de1a9-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="de1a9-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="de1a9-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de1a9-148">Minimum supported client</span></span><br/> | <span data-ttu-id="de1a9-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de1a9-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="de1a9-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de1a9-150">Minimum supported server</span></span><br/> | <span data-ttu-id="de1a9-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de1a9-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="de1a9-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de1a9-152">Namespace</span></span><br/>                | <span data-ttu-id="de1a9-153">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="de1a9-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="de1a9-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de1a9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1a9-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="de1a9-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="de1a9-156">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="de1a9-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

