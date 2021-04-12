---
title: Méthodes de propriété IADsFileShare (IADs. h)
description: Les méthodes de propriété de l’interface IADsFileshare obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsFileShare ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105139"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="7c843-105">Méthodes de propriété IADsFileShare</span><span class="sxs-lookup"><span data-stu-id="7c843-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="7c843-106">Les méthodes de propriété de l’interface [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7c843-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="7c843-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7c843-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7c843-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c843-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7c843-109">**CurrentUserCount**</span><span class="sxs-lookup"><span data-stu-id="7c843-109">**CurrentUserCount**</span></span>
<span data-ttu-id="7c843-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c843-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c843-111">Nombre d’utilisateurs connectés au partage.</span><span class="sxs-lookup"><span data-stu-id="7c843-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="7c843-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c843-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c843-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="7c843-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c843-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c843-114">**Description**</span></span>
<span data-ttu-id="7c843-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c843-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c843-116">Description du partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c843-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="7c843-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c843-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c843-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7c843-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="7c843-119">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="7c843-119">**HostComputer**</span></span>
<span data-ttu-id="7c843-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c843-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c843-121">Référence ADsPath à l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="7c843-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="7c843-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c843-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c843-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7c843-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c843-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="7c843-124">**MaxUserCount**</span></span>
<span data-ttu-id="7c843-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c843-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c843-126">Nombre maximal d’utilisateurs autorisés à accéder au partage à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="7c843-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="7c843-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c843-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c843-128">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="7c843-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c843-129">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="7c843-129">**Path**</span></span>
<span data-ttu-id="7c843-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7c843-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="7c843-131">Chemin d’accès au répertoire partagé du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c843-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="7c843-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7c843-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7c843-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7c843-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="7c843-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c843-134">Examples</span></span>

<span data-ttu-id="7c843-135">Pour accéder aux propriétés des partages de fichiers sur un ordinateur, vous devez d’abord établir une liaison avec le « LanmanServer » sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7c843-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="7c843-136">L’exemple de code suivant montre comment configurer la description et le nombre maximal d’utilisateurs autorisés pour tous les partages de fichiers publics sur l’ordinateur, nommés « monordinateur », dans le domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="7c843-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="7c843-137">L’exemple de code suivant montre comment faire du répertoire C : \\ mondossier existant un partage de fichiers public.</span><span class="sxs-lookup"><span data-stu-id="7c843-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="7c843-138">L’exemple de code suivant convertit le répertoire C : mondossier existant en \\ partage de fichiers public.</span><span class="sxs-lookup"><span data-stu-id="7c843-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="7c843-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c843-139">Requirements</span></span>



| <span data-ttu-id="7c843-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c843-140">Requirement</span></span> | <span data-ttu-id="7c843-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c843-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c843-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c843-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7c843-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c843-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c843-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c843-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7c843-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c843-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c843-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c843-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c843-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c843-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7c843-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7c843-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c843-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c843-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c843-150">IID</span><span class="sxs-lookup"><span data-stu-id="7c843-150">IID</span></span><br/>                      | <span data-ttu-id="7c843-151">IID \_ IADsFileShare est défini en tant que EB6DCAF0-4B83-11CF-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="7c843-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7c843-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c843-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c843-153">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="7c843-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="7c843-154">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="7c843-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="7c843-155">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="7c843-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





