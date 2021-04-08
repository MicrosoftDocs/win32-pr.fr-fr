---
title: Méthodes de propriété IADsO (IADs. h)
description: Les méthodes de propriété de l’interface IADsO obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsO ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742685"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="f8af5-105">Méthodes de propriété IADsO</span><span class="sxs-lookup"><span data-stu-id="f8af5-105">IADsO Property Methods</span></span>

<span data-ttu-id="f8af5-106">Les méthodes de propriété de l’interface [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f8af5-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f8af5-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f8af5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f8af5-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8af5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f8af5-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="f8af5-109">**Description**</span></span>
<span data-ttu-id="f8af5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-111">Description de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="f8af5-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8af5-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8af5-114">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="f8af5-114">**FaxNumber**</span></span>
<span data-ttu-id="f8af5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-116">Numéro de télécopie de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="f8af5-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8af5-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8af5-119">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="f8af5-119">**LocalityName**</span></span>
<span data-ttu-id="f8af5-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-121">Nom de l’emplacement où se trouve l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="f8af5-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8af5-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8af5-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="f8af5-124">**PostalAddress**</span></span>
<span data-ttu-id="f8af5-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-126">Adresse postale de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="f8af5-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8af5-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8af5-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="f8af5-129">**SeeAlso**</span></span>
<span data-ttu-id="f8af5-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-131">Tableau de noms ADsPath d’autres objets ADSI qui peuvent être pertinents pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="f8af5-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="f8af5-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-133">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="f8af5-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8af5-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="f8af5-134">**TelephoneNumber**</span></span>
<span data-ttu-id="f8af5-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f8af5-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="f8af5-136">Numéro de téléphone de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="f8af5-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f8af5-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8af5-138">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8af5-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="f8af5-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="f8af5-139">Examples</span></span>

<span data-ttu-id="f8af5-140">L’exemple de code suivant affiche la description d’une organisation donnée.</span><span class="sxs-lookup"><span data-stu-id="f8af5-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="f8af5-141">Il suppose que le service d’annuaire sous-jacent prend en charge le regroupement d’objets d’annuaire par organisation.</span><span class="sxs-lookup"><span data-stu-id="f8af5-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="f8af5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8af5-142">Requirements</span></span>



| <span data-ttu-id="f8af5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8af5-143">Requirement</span></span> | <span data-ttu-id="f8af5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8af5-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8af5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8af5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f8af5-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8af5-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8af5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8af5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f8af5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8af5-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8af5-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8af5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8af5-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8af5-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f8af5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f8af5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8af5-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8af5-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8af5-153">IID</span><span class="sxs-lookup"><span data-stu-id="f8af5-153">IID</span></span><br/>                      | <span data-ttu-id="f8af5-154">IID \_ IADsO est défini en tant que A1CD2DC6-effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="f8af5-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f8af5-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8af5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8af5-156">**IADsO**</span><span class="sxs-lookup"><span data-stu-id="f8af5-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="f8af5-157">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="f8af5-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





