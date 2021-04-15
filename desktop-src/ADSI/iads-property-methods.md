---
title: Méthodes de propriété IADs (IADs. h)
description: Les méthodes de propriété de l’interface IADss obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508345"
---
# <a name="iads-property-methods"></a><span data-ttu-id="c14c0-105">Méthodes de propriété IADs</span><span class="sxs-lookup"><span data-stu-id="c14c0-105">IADs Property Methods</span></span>

<span data-ttu-id="c14c0-106">Les méthodes de propriété de l’interface [**iadss**](/windows/desktop/api/Iads/nn-iads-iads) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c14c0-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="c14c0-107">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c14c0-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c14c0-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c14c0-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c14c0-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="c14c0-109">**ADsPath**</span></span>
<span data-ttu-id="c14c0-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-111">Chaîne ADsPath de cet objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-111">The ADsPath string of this object.</span></span> <span data-ttu-id="c14c0-112">La chaîne identifie cet objet de manière unique dans un environnement réseau.</span><span class="sxs-lookup"><span data-stu-id="c14c0-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="c14c0-113">L’objet peut toujours être récupéré à l’aide de ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="c14c0-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="c14c0-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-115">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c14c0-116">**Classe**</span><span class="sxs-lookup"><span data-stu-id="c14c0-116">**Class**</span></span>
<span data-ttu-id="c14c0-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-118">Nom de la classe de schéma de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="c14c0-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-120">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c14c0-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c14c0-121">**GUID**</span></span>
<span data-ttu-id="c14c0-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-123">Identificateur global unique de l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c14c0-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="c14c0-124">L’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) convertit le **GUID** d’une chaîne d’octets, telle qu’elle est stockée sur un serveur d’annuaire, en un format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c14c0-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="c14c0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-126">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c14c0-127">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c14c0-127">**Name**</span></span>
<span data-ttu-id="c14c0-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-129">Nom relatif de l’objet, tel que nommé dans le service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c14c0-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="c14c0-130">Ce nom distingue cet objet de ses frères.</span><span class="sxs-lookup"><span data-stu-id="c14c0-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="c14c0-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-132">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c14c0-133">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c14c0-133">**Parent**</span></span>
<span data-ttu-id="c14c0-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-135">Chaîne ADsPath du conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="c14c0-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="c14c0-136">Active Directory n’autorise pas la formation de l’ADsPath d’un objet donné en concaténant les propriétés **parent** et **Name** .</span><span class="sxs-lookup"><span data-stu-id="c14c0-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="c14c0-137">Bien que cette opération puisse fonctionner dans certains fournisseurs, il n’est pas garanti qu’elle fonctionne pour toutes les implémentations.</span><span class="sxs-lookup"><span data-stu-id="c14c0-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="c14c0-138">La validité de l’ADsPath est garantie et doit toujours être utilisée pour récupérer le pointeur d’interface d’un objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="c14c0-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-140">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c14c0-141">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="c14c0-141">**Schema**</span></span>
<span data-ttu-id="c14c0-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c14c0-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="c14c0-143">Chaîne ADsPath de l’objet de classe de schéma de cet objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="c14c0-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c14c0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14c0-145">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c14c0-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="c14c0-146">Notes</span><span class="sxs-lookup"><span data-stu-id="c14c0-146">Remarks</span></span>

<span data-ttu-id="c14c0-147">Dans Active Directory, le **GUID** renvoyé à partir du GUID est une chaîne de caractères hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="c14c0-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="c14c0-148">Utilisez le **GUID** résultant pour effectuer une liaison directe à l’objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="c14c0-149">où xxx est la valeur retournée par la propriété GUID.</span><span class="sxs-lookup"><span data-stu-id="c14c0-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="c14c0-150">Pour plus d’informations, consultez [utilisation d’objectGUID pour la liaison à un objet](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="c14c0-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="c14c0-151">Sachez que si vous utilisez un GUID pour établir une liaison à un objet, la méthode de propriété **ADsPath** retourne des valeurs qui sont différentes des valeurs normales qui seraient retournées si vous avez utilisé un nom unique (DN) pour créer une liaison avec le même objet.</span><span class="sxs-lookup"><span data-stu-id="c14c0-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="c14c0-152">Par exemple, le tableau suivant répertorie les valeurs retournées lors de l’utilisation des deux méthodes de liaison différentes pour effectuer une liaison au même objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c14c0-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="c14c0-153">Lier à l’aide de DN</span><span class="sxs-lookup"><span data-stu-id="c14c0-153">Bind using DN</span></span>                                           | <span data-ttu-id="c14c0-154">Lier à l’aide du GUID</span><span class="sxs-lookup"><span data-stu-id="c14c0-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c14c0-155">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c14c0-155">**Name**</span></span>    | <span data-ttu-id="c14c0-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="c14c0-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="c14c0-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="c14c0-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="c14c0-158">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c14c0-158">**Parent**</span></span>  | <span data-ttu-id="c14c0-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="c14c0-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="c14c0-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="c14c0-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="c14c0-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="c14c0-161">**ADsPath**</span></span> | <span data-ttu-id="c14c0-162">LDAP://server/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="c14c0-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="c14c0-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="c14c0-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="c14c0-164">Le fournisseur Winnt ne prend pas en charge la liaison à l’aide du **GUID** de l’objet et retourne la propriété **GUID** dans un format de chaîne légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="c14c0-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c14c0-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="c14c0-165">Examples</span></span>

<span data-ttu-id="c14c0-166">L’exemple de code suivant montre comment récupérer des données d’objet à l’aide de méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="c14c0-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="c14c0-167">L’exemple de code suivant montre comment récupérer des données d’objet à l’aide de méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="c14c0-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="c14c0-168">L’exemple de code suivant montre comment utiliser les méthodes de propriété de l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="c14c0-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="c14c0-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c14c0-169">Requirements</span></span>



| <span data-ttu-id="c14c0-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c14c0-170">Requirement</span></span> | <span data-ttu-id="c14c0-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="c14c0-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c14c0-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c14c0-172">Minimum supported client</span></span><br/> | <span data-ttu-id="c14c0-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c14c0-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c14c0-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c14c0-174">Minimum supported server</span></span><br/> | <span data-ttu-id="c14c0-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c14c0-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c14c0-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="c14c0-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="c14c0-177"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c14c0-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c14c0-178">DLL</span><span class="sxs-lookup"><span data-stu-id="c14c0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c14c0-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c14c0-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c14c0-180">IID</span><span class="sxs-lookup"><span data-stu-id="c14c0-180">IID</span></span><br/>                      | <span data-ttu-id="c14c0-181">IID \_ IADs est défini en tant que FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="c14c0-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c14c0-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c14c0-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14c0-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="c14c0-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="c14c0-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="c14c0-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

