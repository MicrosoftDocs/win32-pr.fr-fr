---
title: Liaison à un objet à l’aide d’un SID
description: Dans Windows Server 2003, il est possible de lier à un objet à l’aide de l’identificateur de sécurité (SID) de l’objet, ainsi que d’un GUID. Le SID de l’objet est stocké dans l’attribut objectSID. La liaison à un SID ne fonctionne pas sur Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Liaison à un objet à l’aide d’une valeur AD SID
- Active Directory, utiliser, liaison, liaison à un objet à l’aide d’un SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462931"
---
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="00335-107">Liaison à un objet à l’aide d’un SID</span><span class="sxs-lookup"><span data-stu-id="00335-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="00335-108">Dans Windows Server 2003, il est possible de lier à un objet à l’aide de l’identificateur de sécurité (SID) de l’objet, ainsi que d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="00335-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="00335-109">Le SID de l’objet est stocké dans l’attribut **objectSID** .</span><span class="sxs-lookup"><span data-stu-id="00335-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="00335-110">La liaison à un SID ne fonctionne pas sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="00335-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="00335-111">Le fournisseur LDAP pour Active Directory Domain Services fournit une méthode pour établir une liaison à un objet à l’aide du SID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00335-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="00335-112">Le format de la chaîne de liaison est le suivant :</span><span class="sxs-lookup"><span data-stu-id="00335-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="00335-113">Dans cet exemple, « ServerName » est le nom du serveur d’annuaire et « XXXXX » est la représentation sous forme de chaîne de la valeur hexadécimale du SID.</span><span class="sxs-lookup"><span data-stu-id="00335-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="00335-114">Le « servername » est facultatif.</span><span class="sxs-lookup"><span data-stu-id="00335-114">The "servername" is optional.</span></span> <span data-ttu-id="00335-115">La chaîne SID est spécifiée dans un format où chaque caractère de la chaîne est la représentation hexadécimale de chaque octet du SID.</span><span class="sxs-lookup"><span data-stu-id="00335-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="00335-116">Par exemple, si le tableau est :</span><span class="sxs-lookup"><span data-stu-id="00335-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="00335-117">la chaîne de liaison SID serait « &lt; sid = AB14E2 &gt; ».</span><span class="sxs-lookup"><span data-stu-id="00335-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="00335-118">La fonction [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) ne doit pas être utilisée pour convertir le tableau SID en une chaîne, car elle précède chaque caractère d’octet avec une barre oblique inverse, qui n’est pas un format de chaîne de liaison valide.</span><span class="sxs-lookup"><span data-stu-id="00335-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="00335-119">La chaîne SID peut également prendre la forme « &lt; sid = S-x-x-xx-XXXXXXXXXX-XXXXXXXXXX-xxxxxxxx-xxx &gt; », où la partie « S-X-x-xx-XXXXXXXXXX-XXXXXXXXXX-xxxxxxxx-xxx » est identique à la chaîne retournée par la fonction [**ConvertSidToStringSid a**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .</span><span class="sxs-lookup"><span data-stu-id="00335-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="00335-120">Lors de la liaison à l’aide du SID de l’objet, certaines méthodes et propriétés [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="00335-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="00335-121">Les propriétés **IADs** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du SID de l’objet :</span><span class="sxs-lookup"><span data-stu-id="00335-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="00335-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="00335-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="00335-123">**Nom**</span><span class="sxs-lookup"><span data-stu-id="00335-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="00335-124">**Parent**</span><span class="sxs-lookup"><span data-stu-id="00335-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="00335-125">Les méthodes **IADsContainer** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du SID de l’objet :</span><span class="sxs-lookup"><span data-stu-id="00335-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="00335-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="00335-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="00335-127">**Créés**</span><span class="sxs-lookup"><span data-stu-id="00335-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="00335-128">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="00335-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="00335-129">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="00335-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="00335-130">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="00335-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="00335-131">Pour utiliser ces méthodes et propriétés après avoir effectué une liaison à un objet à l’aide du SID d’objet, utilisez la méthode [**IADs. obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le nom unique de l’objet, puis utilisez le nom unique pour effectuer une nouvelle liaison à l’objet.</span><span class="sxs-lookup"><span data-stu-id="00335-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="00335-132">L’exemple de code suivant montre comment convertir un **objectSID** en chaîne pouvant être liée.</span><span class="sxs-lookup"><span data-stu-id="00335-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 