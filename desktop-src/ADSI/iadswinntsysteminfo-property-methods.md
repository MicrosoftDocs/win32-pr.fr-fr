---
title: Méthodes de propriété IADsWinNTSystemInfo (IADs. h)
description: Les méthodes de propriété de l’interface IADsWinNTSystemInfo obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsWinNTSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509898"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="d666e-105">Méthodes de propriété IADsWinNTSystemInfo</span><span class="sxs-lookup"><span data-stu-id="d666e-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="d666e-106">Les méthodes de propriété de l’interface [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d666e-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="d666e-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d666e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d666e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d666e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d666e-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="d666e-109">**ComputerName**</span></span>
<span data-ttu-id="d666e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d666e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d666e-111">Nom de l’ordinateur hôte sur lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d666e-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="d666e-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d666e-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d666e-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d666e-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d666e-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="d666e-114">**DomainName**</span></span>
<span data-ttu-id="d666e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d666e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d666e-116">Nom du domaine auquel appartient l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d666e-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="d666e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d666e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d666e-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d666e-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d666e-119">**MAÎTRES**</span><span class="sxs-lookup"><span data-stu-id="d666e-119">**PDC**</span></span>
<span data-ttu-id="d666e-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d666e-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d666e-121">Nom du contrôleur de domaine principal auquel appartient l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d666e-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="d666e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d666e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d666e-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d666e-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d666e-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d666e-124">**UserName**</span></span>
<span data-ttu-id="d666e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d666e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d666e-126">Nom du compte d’utilisateur sous lequel l’objet **WinNTSystemInfo** est créé.</span><span class="sxs-lookup"><span data-stu-id="d666e-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="d666e-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d666e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d666e-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d666e-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d666e-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="d666e-129">Examples</span></span>

<span data-ttu-id="d666e-130">L’exemple de code C/C++ suivant récupère les informations système WinNT.</span><span class="sxs-lookup"><span data-stu-id="d666e-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="d666e-131">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="d666e-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="d666e-132">L’exemple de code Visual Basic suivant récupère les informations système WinNT.</span><span class="sxs-lookup"><span data-stu-id="d666e-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="d666e-133">L’exemple de code pages Visual Basic Scripting Edition/Active Server suivant récupère les informations système WinNT.</span><span class="sxs-lookup"><span data-stu-id="d666e-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="d666e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d666e-134">Requirements</span></span>



| <span data-ttu-id="d666e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d666e-135">Requirement</span></span> | <span data-ttu-id="d666e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d666e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d666e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d666e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d666e-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d666e-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d666e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d666e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d666e-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d666e-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d666e-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="d666e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d666e-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d666e-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d666e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d666e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d666e-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d666e-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d666e-145">IID</span><span class="sxs-lookup"><span data-stu-id="d666e-145">IID</span></span><br/>                      | <span data-ttu-id="d666e-146">IID \_ IADsWinNTSystemInfo est défini en tant que 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="d666e-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d666e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d666e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d666e-148">**IADsWinNTSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="d666e-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





