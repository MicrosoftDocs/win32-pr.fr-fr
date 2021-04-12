---
title: Méthodes de propriété IADsPathname (IADs. h)
description: Obtient ou définit les propriétés EscapedMode.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPathname ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200566"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="92a15-104">Méthodes de propriété IADsPathname</span><span class="sxs-lookup"><span data-stu-id="92a15-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="92a15-105">Les méthodes de propriété de l’interface [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) obtiennent ou définissent les propriétés **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="92a15-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="92a15-106">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="92a15-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="92a15-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92a15-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="92a15-108">**EscapedMode**</span><span class="sxs-lookup"><span data-stu-id="92a15-108">**EscapedMode**</span></span>
<span data-ttu-id="92a15-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="92a15-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="92a15-110">Examinez ou spécifiez comment les caractères d’échappement sont gérés dans un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="92a15-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="92a15-111">Pour plus d’informations et pour obtenir des options définies, consultez [**\_ \_ \_ enum mode d’échappement ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="92a15-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="92a15-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="92a15-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92a15-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="92a15-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="92a15-114">Notes</span><span class="sxs-lookup"><span data-stu-id="92a15-114">Remarks</span></span>

<span data-ttu-id="92a15-115">**EscapedMode** représente un État.</span><span class="sxs-lookup"><span data-stu-id="92a15-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="92a15-116">Vous pouvez l’activer ou la désactiver, en le définissant sur ADS \_ ESCAPEDMODE \_ sur ou publicités \_ ESCAPEDMODE \_ /annonces \_ ESCAPEDMODE \_ OFF \_ .</span><span class="sxs-lookup"><span data-stu-id="92a15-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="92a15-117">Lorsqu’elle est activée ou désactivée, toutes les récupérations suivantes produisent des chaînes de chemin d’accès sans séquence d’échappement ou de séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="92a15-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="92a15-118">Dans ADSI uniquement, le [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) est en charge de l’échappement des chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="92a15-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="92a15-119">Toutes les autres interfaces ADSI retournent toujours des chemins d’échappement.</span><span class="sxs-lookup"><span data-stu-id="92a15-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="92a15-120">L’État par défaut de **EscapedMode** est ADS \_ EscapedMode \_ par défaut, comme défini dans l' [**\_ \_ \_ énumération du mode d’échappement ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="92a15-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="92a15-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="92a15-121">Examples</span></span>

<span data-ttu-id="92a15-122">L’exemple de code suivant montre comment utiliser la propriété **EscapedMode** pour activer/désactiver l’échappement des trois caractères spéciaux suivants : « = », « , » et « / ».</span><span class="sxs-lookup"><span data-stu-id="92a15-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="92a15-123">L’exemple de code suivant montre comment utiliser la propriété **EscapedMode** pour activer/désactiver l’échappement des trois caractères spéciaux suivants : « = », « , » et « / ».</span><span class="sxs-lookup"><span data-stu-id="92a15-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="92a15-124">L’exemple de code suivant montre comment utiliser la propriété **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="92a15-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="92a15-125">La vérification des erreurs est ignorée.</span><span class="sxs-lookup"><span data-stu-id="92a15-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="92a15-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92a15-126">Requirements</span></span>



| <span data-ttu-id="92a15-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92a15-127">Requirement</span></span> | <span data-ttu-id="92a15-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="92a15-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92a15-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="92a15-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92a15-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92a15-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="92a15-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92a15-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92a15-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="92a15-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a15-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a15-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="92a15-135">DLL</span><span class="sxs-lookup"><span data-stu-id="92a15-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a15-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a15-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="92a15-137">IID</span><span class="sxs-lookup"><span data-stu-id="92a15-137">IID</span></span><br/>                      | <span data-ttu-id="92a15-138">IID \_ IADsPathname est défini en tant que D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="92a15-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="92a15-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a15-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a15-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="92a15-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="92a15-141">**\_ \_ énumération du mode d’échappement ADS \_**</span><span class="sxs-lookup"><span data-stu-id="92a15-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





