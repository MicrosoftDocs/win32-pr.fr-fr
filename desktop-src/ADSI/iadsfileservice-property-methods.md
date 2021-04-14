---
title: Méthodes de propriété IADsFileService (IADs. h)
description: Les méthodes de propriété de l’interface IADsFileService obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsFileService ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509030"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="c7e65-105">Méthodes de propriété IADsFileService</span><span class="sxs-lookup"><span data-stu-id="c7e65-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="c7e65-106">Les méthodes de propriété de l’interface [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c7e65-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="c7e65-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c7e65-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c7e65-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7e65-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c7e65-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="c7e65-109">**Description**</span></span>
<span data-ttu-id="c7e65-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c7e65-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c7e65-111">Description du service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c7e65-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="c7e65-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c7e65-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7e65-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c7e65-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="c7e65-114">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="c7e65-114">**MaxUserCount**</span></span>
<span data-ttu-id="c7e65-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c7e65-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c7e65-116">Nombre maximal d’utilisateurs autorisés sur le service à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c7e65-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="c7e65-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c7e65-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7e65-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="c7e65-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="c7e65-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c7e65-119">Remarks</span></span>

<span data-ttu-id="c7e65-120">Vous devez passer par le service de fichiers pour accéder aux partages de fichiers, aux sessions et aux ressources d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c7e65-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="c7e65-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c7e65-121">Examples</span></span>

<span data-ttu-id="c7e65-122">L’exemple de code suivant écrit une description de et vérifie la limite utilisateur du service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c7e65-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="c7e65-123">L’exemple de code suivant écrit une description de et vérifie la limite utilisateur sur un objet de service de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c7e65-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="c7e65-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7e65-124">Requirements</span></span>



| <span data-ttu-id="c7e65-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7e65-125">Requirement</span></span> | <span data-ttu-id="c7e65-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7e65-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e65-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7e65-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e65-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7e65-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7e65-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7e65-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e65-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7e65-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7e65-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7e65-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e65-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e65-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c7e65-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c7e65-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7e65-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7e65-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7e65-135">IID</span><span class="sxs-lookup"><span data-stu-id="c7e65-135">IID</span></span><br/>                      | <span data-ttu-id="c7e65-136">IID \_ IADsFileService est défini en tant que A89D1900-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="c7e65-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c7e65-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7e65-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e65-138">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="c7e65-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="c7e65-139">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="c7e65-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="c7e65-140">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="c7e65-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="c7e65-141">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="c7e65-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="c7e65-142">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="c7e65-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





