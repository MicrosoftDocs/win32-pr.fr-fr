---
title: Méthodes de propriété IADsOU (IADs. h)
description: Les méthodes de propriété de l’interface IADsOU obtiennent ou définissent les propriétés énumérées dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsOU ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512822"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="98779-105">Méthodes de propriété IADsOU</span><span class="sxs-lookup"><span data-stu-id="98779-105">IADsOU Property Methods</span></span>

<span data-ttu-id="98779-106">Les méthodes de propriété de l’interface [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) obtiennent ou définissent les propriétés énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="98779-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="98779-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="98779-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="98779-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98779-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="98779-109">**BusinessCategory**</span><span class="sxs-lookup"><span data-stu-id="98779-109">**BusinessCategory**</span></span>
<span data-ttu-id="98779-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-111">Chaîne qui contient la fonction commerciale générale ou les fonctions effectuées par l’unité d’organisation, par exemple « comptabilité ».</span><span class="sxs-lookup"><span data-stu-id="98779-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="98779-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="98779-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="98779-114">**Description**</span></span>
<span data-ttu-id="98779-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-116">Chaîne qui contient une description textuelle de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="98779-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="98779-119">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="98779-119">**FaxNumber**</span></span>
<span data-ttu-id="98779-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-121">Chaîne qui contient le numéro de télécopie de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="98779-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="98779-124">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="98779-124">**LocalityName**</span></span>
<span data-ttu-id="98779-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-126">Chaîne qui contient le nom de la région géographique de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="98779-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="98779-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="98779-129">**PostalAddress**</span></span>
<span data-ttu-id="98779-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-131">Chaîne qui contient l’adresse postale de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="98779-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-133">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="98779-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="98779-134">**SeeAlso**</span></span>
<span data-ttu-id="98779-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-136">Tableau de chaînes qui contient les noms uniques des autres objets d’annuaire qui peuvent être pertinents pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="98779-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="98779-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-138">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="98779-138">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="98779-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="98779-139">**TelephoneNumber**</span></span>
<span data-ttu-id="98779-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="98779-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="98779-141">Chaîne qui contient le numéro de téléphone de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="98779-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="98779-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="98779-143">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="98779-143">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="98779-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="98779-144">Examples</span></span>

<span data-ttu-id="98779-145">L’exemple de code suivant affiche le **BusinessCategory** et la **Description** de toutes les unités d’organisation dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="98779-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="98779-146">Il part du principe que le service d’annuaire sous-jacent prend en charge le regroupement d’objets d’annuaire par unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="98779-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="98779-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98779-147">Requirements</span></span>



| <span data-ttu-id="98779-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98779-148">Requirement</span></span> | <span data-ttu-id="98779-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="98779-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98779-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98779-150">Minimum supported client</span></span><br/> | <span data-ttu-id="98779-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98779-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98779-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98779-152">Minimum supported server</span></span><br/> | <span data-ttu-id="98779-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98779-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98779-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="98779-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="98779-155"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="98779-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="98779-156">DLL</span><span class="sxs-lookup"><span data-stu-id="98779-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98779-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98779-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="98779-158">IID</span><span class="sxs-lookup"><span data-stu-id="98779-158">IID</span></span><br/>                      | <span data-ttu-id="98779-159">IID \_ IADsOU est défini en tant que A2F733B8-effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="98779-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="98779-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98779-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98779-161">**IADsOU**</span><span class="sxs-lookup"><span data-stu-id="98779-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="98779-162">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="98779-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





