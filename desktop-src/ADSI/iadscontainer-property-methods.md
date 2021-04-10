---
title: Méthodes de propriété IADsContainer (IADs. h)
description: Les méthodes de propriété de l’interface IADsContainer obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105151"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="67040-105">Méthodes de propriété IADsContainer</span><span class="sxs-lookup"><span data-stu-id="67040-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="67040-106">Les méthodes de propriété de l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="67040-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="67040-107">Pour plus d’informations et pour obtenir une discussion générale sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="67040-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="67040-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67040-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="67040-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="67040-109">**Count**</span></span>
<span data-ttu-id="67040-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67040-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="67040-111">Récupère le nombre d’éléments dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="67040-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="67040-112">Quand le **filtre** est défini, **Count** retourne uniquement le nombre d’éléments filtrés.</span><span class="sxs-lookup"><span data-stu-id="67040-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="67040-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67040-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67040-114">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="67040-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="67040-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="67040-115">**Filter**</span></span>
<span data-ttu-id="67040-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67040-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="67040-117">Récupère ou définit le filtre utilisé pour sélectionner des classes d’objet dans une énumération donnée.</span><span class="sxs-lookup"><span data-stu-id="67040-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="67040-118">Il s’agit d’un tableau variant, dont chaque élément est le nom d’une classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="67040-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="67040-119">Si le **filtre** n’est pas défini ou n’est pas défini sur vide, tous les objets de toutes les classes sont récupérés par l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="67040-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="67040-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67040-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="67040-121">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="67040-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="67040-122">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="67040-122">**Hints**</span></span>
<span data-ttu-id="67040-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="67040-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="67040-124">Tableau de variant de chaînes **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="67040-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="67040-125">Chaque élément identifie le nom d’une propriété trouvée dans la définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="67040-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="67040-126">Le paramètre *vHints* permet au client d’indiquer les attributs à charger pour chaque objet énuméré.</span><span class="sxs-lookup"><span data-stu-id="67040-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="67040-127">Ces données peuvent être utilisées pour optimiser l’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="67040-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="67040-128">L’implémentation exacte, toutefois, est spécifique au fournisseur et n’est actuellement pas utilisée par le fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="67040-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="67040-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67040-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="67040-130">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="67040-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="67040-131">Notes</span><span class="sxs-lookup"><span data-stu-id="67040-131">Remarks</span></span>

<span data-ttu-id="67040-132">Les processus d’énumération sous [**IADsContainer :: obten \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) et **IADsContainer :: obtient \_ Count** sont effectués sur les objets contenus dans le cache.</span><span class="sxs-lookup"><span data-stu-id="67040-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="67040-133">Lorsqu’un conteneur contient un grand nombre d’objets, les performances peuvent être affectées.</span><span class="sxs-lookup"><span data-stu-id="67040-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="67040-134">Pour améliorer les performances, désactivez le cache, configurez une taille de page appropriée et utilisez l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="67040-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="67040-135">Pour cette raison, la propriété **obtenir le \_ nombre** n’est pas prise en charge dans le fournisseur LDAP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67040-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="67040-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="67040-136">Examples</span></span>

<span data-ttu-id="67040-137">L’exemple de code Visual Basic suivant montre comment les méthodes de propriété de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="67040-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="67040-138">L’exemple de code C++ suivant montre comment les méthodes de propriété de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="67040-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="67040-139">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="67040-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="67040-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67040-140">Requirements</span></span>



| <span data-ttu-id="67040-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67040-141">Requirement</span></span> | <span data-ttu-id="67040-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="67040-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67040-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67040-143">Minimum supported client</span></span><br/> | <span data-ttu-id="67040-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67040-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67040-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67040-145">Minimum supported server</span></span><br/> | <span data-ttu-id="67040-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67040-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67040-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="67040-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="67040-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="67040-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="67040-149">DLL</span><span class="sxs-lookup"><span data-stu-id="67040-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67040-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67040-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="67040-151">IID</span><span class="sxs-lookup"><span data-stu-id="67040-151">IID</span></span><br/>                      | <span data-ttu-id="67040-152">IID \_ IADsContainer est défini en tant que 001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="67040-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="67040-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67040-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67040-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="67040-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="67040-155">**Rubrique IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="67040-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





