---
description: Définit le descripteur de sécurité pour l’espace de noms auquel un utilisateur est connecté. Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Méthode configured de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523241"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="c061a-105">Méthode configured de la \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="c061a-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="c061a-106">La méthode **configured** définit le descripteur de sécurité pour l’espace de noms auquel un utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="c061a-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="c061a-107">Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="c061a-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="c061a-108">Si vous écrivez un script, utilisez la méthode [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="c061a-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="c061a-109">Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="c061a-110">Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide de [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="c061a-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="c061a-111">Un utilisateur doit disposer de l’autorisation **Write \_ DAC** et, par défaut, un administrateur dispose de cette autorisation.</span><span class="sxs-lookup"><span data-stu-id="c061a-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="c061a-112">La seule partie du descripteur de sécurité utilisée est l’entrée de contrôle d’accès (ACE) non héritée dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="c061a-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="c061a-113">En définissant l’indicateur **conteneur d' \_ héritage** dans les ACE, le descripteur de sécurité affecte les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="c061a-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="c061a-114">Les ACE allow et Deny sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="c061a-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="c061a-115">Étant donné que les ACE Deny et allow sont toutes deux autorisées dans une liste DACL, l’ordre des ACE est important.</span><span class="sxs-lookup"><span data-stu-id="c061a-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="c061a-116">Pour plus d’informations, consultez [classement des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="c061a-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c061a-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c061a-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="c061a-118">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c061a-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c061a-119">*SD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c061a-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c061a-120">Tableau d’octets qui compose le descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c061a-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c061a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c061a-121">Return value</span></span>

<span data-ttu-id="c061a-122">Retourne un **HRESULT** qui indique l’état d’un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="c061a-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="c061a-123">Pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="c061a-124">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="c061a-125">La liste suivante répertorie les valeurs de retour qui sont significatives pour les **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="c061a-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="c061a-126">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="c061a-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="c061a-127">Méthode exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c061a-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="c061a-128">**\_accès WBEM \_ E \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="c061a-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="c061a-129">L’appelant ne dispose pas des droits suffisants pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c061a-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="c061a-130">**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="c061a-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="c061a-131">Tentative d’exécution de cette méthode sur le système d’exploitation qui ne la prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="c061a-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="c061a-132">**WBEM \_ E \_ objet non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c061a-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="c061a-133">SD ne passe pas les tests de validité de base.</span><span class="sxs-lookup"><span data-stu-id="c061a-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="c061a-134">**\_paramètre WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="c061a-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="c061a-135">SD n’est pas valide en raison de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c061a-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="c061a-136">DACL est manquant.</span><span class="sxs-lookup"><span data-stu-id="c061a-136">DACL is missing.</span></span>
-   <span data-ttu-id="c061a-137">DACL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c061a-137">DACL is not valid.</span></span>
-   <span data-ttu-id="c061a-138">L’entrée de contrôle d’accès est associée à l’indicateur **WBEM \_ Full \_ Write \_ REP** et l’indicateur **WBEM écriture \_ partielle \_ \_ WBEM** ou **\_ \_ fournisseur d’écriture WBEM** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="c061a-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="c061a-139">L’entrée du contrôle d’accès a l’indicateur **\_ \_ ACE inherit only** défini sans l’indicateur **\_ \_ ACE inherit du conteneur** .</span><span class="sxs-lookup"><span data-stu-id="c061a-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="c061a-140">L’ACE a un jeu de bits d’accès inconnu.</span><span class="sxs-lookup"><span data-stu-id="c061a-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="c061a-141">L’ACE a un indicateur défini qui ne figure pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="c061a-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="c061a-142">Le type de l’entrée du contrôle d’accès n’est pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="c061a-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="c061a-143">Le propriétaire et le groupe sont absents du SD.</span><span class="sxs-lookup"><span data-stu-id="c061a-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="c061a-144">Pour plus d’informations sur les indicateurs d’entrée de contrôle d’accès (ACE), consultez [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c061a-145">Notes</span><span class="sxs-lookup"><span data-stu-id="c061a-145">Remarks</span></span>

<span data-ttu-id="c061a-146">Pour plus d’informations sur la modification de la sécurité des espaces de noms par programmation ou manuelle, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="c061a-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c061a-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="c061a-147">Examples</span></span>

<span data-ttu-id="c061a-148">Le script suivant montre comment utiliser SETD pour définir le descripteur **de sécurité** de l’espace de noms pour l’espace de noms racine et le remplacer par le tableau d’octets affiché dans *strSD*.</span><span class="sxs-lookup"><span data-stu-id="c061a-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="c061a-149">L’exemple de code C# suivant utilise System. Security. AccessControl. RawSecurityDescriptor pour énumérer, insérer et supprimer de nouveaux objets CommonAce dans RawSecurityDescriptor. DiscretionaryAcl, puis le reconvertir en tableau d’octets pour l’enregistrer via le paramètre.</span><span class="sxs-lookup"><span data-stu-id="c061a-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="c061a-150">Un SecurityIdentifier peut être récupéré à l’aide de NTAccount et de translate.</span><span class="sxs-lookup"><span data-stu-id="c061a-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="c061a-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c061a-151">Requirements</span></span>



| <span data-ttu-id="c061a-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c061a-152">Requirement</span></span> | <span data-ttu-id="c061a-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c061a-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c061a-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c061a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c061a-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c061a-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c061a-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c061a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c061a-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c061a-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c061a-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c061a-158">Namespace</span></span><br/>                | <span data-ttu-id="c061a-159">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="c061a-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c061a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c061a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c061a-161">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="c061a-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c061a-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="c061a-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="c061a-163">**\_\_SystemSecurity :: est**</span><span class="sxs-lookup"><span data-stu-id="c061a-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="c061a-164">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="c061a-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="c061a-165">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="c061a-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="c061a-166">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="c061a-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="c061a-167">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="c061a-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

