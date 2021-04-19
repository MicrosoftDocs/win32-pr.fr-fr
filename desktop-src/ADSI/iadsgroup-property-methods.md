---
title: Méthodes de propriété IADsGroup (IADs. h)
description: Méthodes de propriété de l’interface IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515073"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="384f2-104">Méthodes de propriété IADsGroup</span><span class="sxs-lookup"><span data-stu-id="384f2-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="384f2-105">Les méthodes de propriété de l’interface [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) lisent et écrivent les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="384f2-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="384f2-106">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="384f2-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="384f2-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="384f2-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="384f2-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="384f2-108">**Description**</span></span>
<span data-ttu-id="384f2-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="384f2-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="384f2-110">Indique la description textuelle de l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="384f2-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="384f2-111">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="384f2-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="384f2-112">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="384f2-112">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="384f2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="384f2-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="384f2-114">Utilisation de IADsGroup pour récupérer les descriptions des groupes prédéfinis</span><span class="sxs-lookup"><span data-stu-id="384f2-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="384f2-115">Les exemples suivants montrent comment récupérer des informations sur les objets de groupe Windows par nom.</span><span class="sxs-lookup"><span data-stu-id="384f2-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="384f2-116">Dans un environnement multilingue, les groupes intégrés sont parfois connus par différents noms localisés, ce qui signifie qu’ils ne peuvent pas être récupérés directement à l’aide d’identificateurs de chaîne tels que « WinNT://Microsoft/Administrators ».</span><span class="sxs-lookup"><span data-stu-id="384f2-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="384f2-117">Dans ce cas, l’utilisateur peut effectuer une liaison à l’objet SID connu pour le groupe, récupérer le nom de groupe localisé et le fournir à la méthode GetObject.</span><span class="sxs-lookup"><span data-stu-id="384f2-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="384f2-118">Pour plus d’informations, consultez [sid connus](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="384f2-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="384f2-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="384f2-119">Examples</span></span>

<span data-ttu-id="384f2-120">L’exemple de Visual Basic suivant montre comment effectuer une liaison à un objet de groupe et afficher la description du groupe.</span><span class="sxs-lookup"><span data-stu-id="384f2-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="384f2-121">L’exemple C++ suivant montre comment effectuer une liaison à un objet de groupe et afficher la description du groupe.</span><span class="sxs-lookup"><span data-stu-id="384f2-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="384f2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="384f2-122">Requirements</span></span>



| <span data-ttu-id="384f2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="384f2-123">Requirement</span></span> | <span data-ttu-id="384f2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="384f2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="384f2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="384f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="384f2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="384f2-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="384f2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="384f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="384f2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="384f2-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="384f2-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="384f2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="384f2-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="384f2-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="384f2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="384f2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="384f2-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="384f2-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="384f2-133">IID</span><span class="sxs-lookup"><span data-stu-id="384f2-133">IID</span></span><br/>                      | <span data-ttu-id="384f2-134">IID \_ IADsGroup est défini en tant que 27636B00-410f-11CF-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="384f2-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="384f2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="384f2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="384f2-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="384f2-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="384f2-137">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="384f2-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="384f2-138">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="384f2-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

