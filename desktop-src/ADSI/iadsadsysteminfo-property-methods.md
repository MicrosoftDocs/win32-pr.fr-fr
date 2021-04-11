---
title: Méthodes de propriété IADsADSystemInfo (IADs. h)
description: Les méthodes de propriété de l’interface IADsADSystemInfo obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsADSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105166"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="4df75-105">Méthodes de propriété IADsADSystemInfo</span><span class="sxs-lookup"><span data-stu-id="4df75-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="4df75-106">Les méthodes de propriété de l’interface [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) obtiennent ou définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4df75-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="4df75-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4df75-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4df75-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4df75-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4df75-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="4df75-109">**ComputerName**</span></span>
<span data-ttu-id="4df75-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-111">Récupère le nom unique de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4df75-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="4df75-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-114">**DomainDNSName**</span><span class="sxs-lookup"><span data-stu-id="4df75-114">**DomainDNSName**</span></span>
<span data-ttu-id="4df75-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-116">Récupère le nom DNS du domaine de l’ordinateur local, tel que « domainName.companyName.com ».</span><span class="sxs-lookup"><span data-stu-id="4df75-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="4df75-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-119">**DomainShortName**</span><span class="sxs-lookup"><span data-stu-id="4df75-119">**DomainShortName**</span></span>
<span data-ttu-id="4df75-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-121">Récupère le nom abrégé du domaine de l’ordinateur local, tel que « nom_domaine ».</span><span class="sxs-lookup"><span data-stu-id="4df75-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="4df75-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="4df75-124">**ForestDNSName**</span></span>
<span data-ttu-id="4df75-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-126">Récupère le nom DNS de la forêt de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4df75-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="4df75-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-129">**IsNativeMode**</span><span class="sxs-lookup"><span data-stu-id="4df75-129">**IsNativeMode**</span></span>
<span data-ttu-id="4df75-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-131">Détermine si le domaine de l’ordinateur local est en mode natif ou mixte.</span><span class="sxs-lookup"><span data-stu-id="4df75-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="4df75-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-133">Type de données de script : **bool**</span><span class="sxs-lookup"><span data-stu-id="4df75-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-134">**PDCRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="4df75-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="4df75-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-136">Récupère le nom unique de l’objet agent du service d’annuaire (DSA) pour le contrôleur de domaine qui possède le rôle de contrôleur de domaine principal dans le domaine de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4df75-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="4df75-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-138">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="4df75-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="4df75-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-141">Récupère le nom unique de l’objet agent du service d’annuaire (DSA) pour le contrôleur de bus qui détient le rôle de contrôleur de schéma dans la forêt de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4df75-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="4df75-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-143">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-144">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="4df75-144">**SiteName**</span></span>
<span data-ttu-id="4df75-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-146">Récupère le nom de site de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4df75-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="4df75-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-148">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4df75-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="4df75-149">**UserName**</span></span>
<span data-ttu-id="4df75-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4df75-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="4df75-151">Récupère le Active Directory nom unique de l’utilisateur actuel, qui est l’utilisateur connecté ou l’utilisateur représenté par le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="4df75-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="4df75-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4df75-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4df75-153">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4df75-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4df75-154">Exemples</span><span class="sxs-lookup"><span data-stu-id="4df75-154">Examples</span></span>

<span data-ttu-id="4df75-155">L’exemple de code C++ suivant récupère les informations système Windows.</span><span class="sxs-lookup"><span data-stu-id="4df75-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="4df75-156">Par souci de concision, la vérification des erreurs est omise.</span><span class="sxs-lookup"><span data-stu-id="4df75-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="4df75-157">L’exemple de code Visual Basic suivant récupère les informations système Windows.</span><span class="sxs-lookup"><span data-stu-id="4df75-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="4df75-158">L’exemple de code VBScript/ASP suivant récupère les informations système Windows.</span><span class="sxs-lookup"><span data-stu-id="4df75-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="4df75-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4df75-159">Requirements</span></span>



| <span data-ttu-id="4df75-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4df75-160">Requirement</span></span> | <span data-ttu-id="4df75-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="4df75-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df75-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df75-162">Minimum supported client</span></span><br/> | <span data-ttu-id="4df75-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4df75-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4df75-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df75-164">Minimum supported server</span></span><br/> | <span data-ttu-id="4df75-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4df75-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4df75-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="4df75-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df75-167"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df75-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4df75-168">DLL</span><span class="sxs-lookup"><span data-stu-id="4df75-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4df75-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4df75-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4df75-170">IID</span><span class="sxs-lookup"><span data-stu-id="4df75-170">IID</span></span><br/>                      | <span data-ttu-id="4df75-171">IID \_ IADsADSystemInfo est défini en tant que 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="4df75-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="4df75-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df75-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df75-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="4df75-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="4df75-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="4df75-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

