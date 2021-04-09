---
title: Méthodes de propriété IADsSecurityDescriptor (IADs. h)
description: Les méthodes de propriété de l’interface IADsSecurityDescriptor obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsSecurityDescriptor ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103497"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="1dc58-105">Méthodes de propriété IADsSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="1dc58-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="1dc58-106">Les méthodes de propriété de l’interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1dc58-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="1dc58-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1dc58-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1dc58-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1dc58-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1dc58-109">**Contrôle**</span><span class="sxs-lookup"><span data-stu-id="1dc58-109">**Control**</span></span>
<span data-ttu-id="1dc58-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-111">Indicateurs qui qualifient la signification du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="1dc58-112">Les valeurs sont extraites de la structure de [**\_ \_ contrôle du descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.</span><span class="sxs-lookup"><span data-stu-id="1dc58-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="1dc58-113">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-114">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="1dc58-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-115">**DaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="1dc58-115">**DaclDefaulted**</span></span>
<span data-ttu-id="1dc58-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-117">Indicateur du type BOOL qui indique si la liste DACL est dérivée d’un mécanisme par défaut, plutôt que d’être fournie explicitement par le fournisseur d’origine du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="1dc58-118">Par exemple, si le créateur d’un objet ne spécifie pas de liste DACL, l’objet reçoit la DACL par défaut à partir du jeton d’accès du créateur.</span><span class="sxs-lookup"><span data-stu-id="1dc58-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="1dc58-119">Cet indicateur peut affecter la façon dont le système traite la liste DACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="1dc58-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="1dc58-120">Le système ignore cet indicateur si l' \_ indicateur de \_ présence DACL se présente n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1dc58-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="1dc58-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-122">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1dc58-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-123">**DiscretionaryAcl**</span><span class="sxs-lookup"><span data-stu-id="1dc58-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="1dc58-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-125">Liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) qui spécifie les types d’accès accordés à l’objet pour les utilisateurs et les groupes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1dc58-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="1dc58-126">Pour plus d’informations sur les DACL, consultez [DACL null et listes DACL vides](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="1dc58-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="1dc58-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-128">Type de données de script : **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1dc58-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-129">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="1dc58-129">**Group**</span></span>
<span data-ttu-id="1dc58-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-131">Groupe auquel appartient l’ID de sécurité du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1dc58-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="1dc58-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1dc58-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-134">**GroupDefaulted**</span><span class="sxs-lookup"><span data-stu-id="1dc58-134">**GroupDefaulted**</span></span>
<span data-ttu-id="1dc58-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-136">Indicateur du type BOOL qui indique si les données de groupe sont dérivées d’un mécanisme par défaut, plutôt que d’être explicitement fournies par le fournisseur d’origine du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="1dc58-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-138">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1dc58-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-139">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="1dc58-139">**Owner**</span></span>
<span data-ttu-id="1dc58-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-141">Propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1dc58-141">Object owner.</span></span>

<dt>

<span data-ttu-id="1dc58-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-143">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1dc58-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-144">**OwnerDefaulted**</span><span class="sxs-lookup"><span data-stu-id="1dc58-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="1dc58-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-146">Indicateur du type BOOL qui indique que les données de propriétaire sont dérivées d’un mécanisme par défaut, plutôt que d’être explicitement fournies par le fournisseur d’origine du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="1dc58-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-148">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1dc58-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-149">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="1dc58-149">**Revision**</span></span>
<span data-ttu-id="1dc58-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-151">Niveau de révision du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="1dc58-152">Cette valeur est extraite de la structure des [**\_ \_ informations de révision**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) de la liste de contrôle d’accès Win32.</span><span class="sxs-lookup"><span data-stu-id="1dc58-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="1dc58-153">Toutes les entrées du contrôle d’accès d’une liste de contrôle d’accès doivent être au même niveau de révision.</span><span class="sxs-lookup"><span data-stu-id="1dc58-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="1dc58-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-155">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="1dc58-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-156">**SaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="1dc58-156">**SaclDefaulted**</span></span>
<span data-ttu-id="1dc58-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-158">Indicateur du type BOOL qui indique que la liste SACL est dérivée d’un mécanisme par défaut, plutôt que d’être explicitement fournie par le fournisseur d’origine du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1dc58-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="1dc58-159">Cet indicateur peut affecter la façon dont le système gère la liste SACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="1dc58-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="1dc58-160">Le système ignore cet indicateur si l' \_ indicateur de \_ présence SACL se présente n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1dc58-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="1dc58-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-162">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1dc58-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dc58-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="1dc58-163">**SystemAcl**</span></span>
<span data-ttu-id="1dc58-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dc58-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dc58-165">Liste de contrôle d’accès système utilisée pour générer des enregistrements d’audit pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="1dc58-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="1dc58-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dc58-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dc58-167">Type de données de script : **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1dc58-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="1dc58-168">Exemples</span><span class="sxs-lookup"><span data-stu-id="1dc58-168">Examples</span></span>

<span data-ttu-id="1dc58-169">L’exemple de code suivant montre comment énumérer un descripteur de sécurité existant.</span><span class="sxs-lookup"><span data-stu-id="1dc58-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="1dc58-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1dc58-170">Requirements</span></span>



| <span data-ttu-id="1dc58-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dc58-171">Requirement</span></span> | <span data-ttu-id="1dc58-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dc58-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc58-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dc58-173">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc58-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dc58-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="1dc58-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dc58-175">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc58-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dc58-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1dc58-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="1dc58-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc58-178"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc58-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="1dc58-179">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc58-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc58-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc58-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1dc58-181">IID</span><span class="sxs-lookup"><span data-stu-id="1dc58-181">IID</span></span><br/>                      | <span data-ttu-id="1dc58-182">IID \_ IADsSecurityDescriptor est défini en tant que B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="1dc58-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1dc58-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dc58-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc58-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1dc58-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="1dc58-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="1dc58-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="1dc58-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="1dc58-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

