---
title: Méthodes de propriété IADsLocality (IADs. h)
description: Les méthodes de l’interface IADsLocality lisent et écrivent les propriétés décrites dans cette rubrique. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsLocality ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942569"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="a895b-105">Méthodes de propriété IADsLocality</span><span class="sxs-lookup"><span data-stu-id="a895b-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="a895b-106">Les méthodes de l’interface [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) lisent et écrivent les propriétés décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a895b-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="a895b-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a895b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a895b-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a895b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a895b-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="a895b-109">**Description**</span></span>
<span data-ttu-id="a895b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a895b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="a895b-111">Indique le texte qui décrit la localité.</span><span class="sxs-lookup"><span data-stu-id="a895b-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="a895b-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a895b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a895b-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a895b-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="a895b-114">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="a895b-114">**LocalityName**</span></span>
<span data-ttu-id="a895b-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a895b-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="a895b-116">Indique le nom de la région géographique, tel qu’il est représenté par cet objet de localité.</span><span class="sxs-lookup"><span data-stu-id="a895b-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="a895b-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a895b-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a895b-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a895b-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="a895b-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="a895b-119">**PostalAddress**</span></span>
<span data-ttu-id="a895b-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a895b-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="a895b-121">Indique l’adresse postale principale de la localité.</span><span class="sxs-lookup"><span data-stu-id="a895b-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="a895b-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a895b-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a895b-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a895b-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="a895b-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="a895b-124">**SeeAlso**</span></span>
<span data-ttu-id="a895b-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a895b-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="a895b-126">Indique un tableau de noms ADsPath d’objets d’annuaire en rapport avec cet objet.</span><span class="sxs-lookup"><span data-stu-id="a895b-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="a895b-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a895b-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a895b-128">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="a895b-128">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a895b-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="a895b-129">Examples</span></span>

<span data-ttu-id="a895b-130">L’exemple de code suivant affiche les données de localité d’un objet conteneur.</span><span class="sxs-lookup"><span data-stu-id="a895b-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="a895b-131">Il part du principe qu’un objet de localité, nommé « myLocality », a été créé pour l’objet conteneur et que les propriétés ont été définies.</span><span class="sxs-lookup"><span data-stu-id="a895b-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="a895b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a895b-132">Requirements</span></span>



| <span data-ttu-id="a895b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a895b-133">Requirement</span></span> | <span data-ttu-id="a895b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a895b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a895b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a895b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a895b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a895b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a895b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a895b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a895b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a895b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a895b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="a895b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a895b-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a895b-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a895b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a895b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a895b-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a895b-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a895b-143">IID</span><span class="sxs-lookup"><span data-stu-id="a895b-143">IID</span></span><br/>                      | <span data-ttu-id="a895b-144">IID \_ IADsLocality est défini en tant que A05E03A2-effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="a895b-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a895b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a895b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a895b-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="a895b-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="a895b-147">**IADsLocality**</span><span class="sxs-lookup"><span data-stu-id="a895b-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="a895b-148">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="a895b-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





