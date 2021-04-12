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
# <a name="binding-to-an-object-using-a-sid"></a>Liaison à un objet à l’aide d’un SID

Dans Windows Server 2003, il est possible de lier à un objet à l’aide de l’identificateur de sécurité (SID) de l’objet, ainsi que d’un GUID. Le SID de l’objet est stocké dans l’attribut **objectSID** . La liaison à un SID ne fonctionne pas sur Windows 2000.

Le fournisseur LDAP pour Active Directory Domain Services fournit une méthode pour établir une liaison à un objet à l’aide du SID de l’objet. Le format de la chaîne de liaison est le suivant :


```C++
LDAP://servername/<SID=XXXXX>
```



Dans cet exemple, « ServerName » est le nom du serveur d’annuaire et « XXXXX » est la représentation sous forme de chaîne de la valeur hexadécimale du SID. Le « servername » est facultatif. La chaîne SID est spécifiée dans un format où chaque caractère de la chaîne est la représentation hexadécimale de chaque octet du SID. Par exemple, si le tableau est :


```C++
0xAB 0x14 0xE2
```



la chaîne de liaison SID serait « &lt; sid = AB14E2 &gt; ». La fonction [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) ne doit pas être utilisée pour convertir le tableau SID en une chaîne, car elle précède chaque caractère d’octet avec une barre oblique inverse, qui n’est pas un format de chaîne de liaison valide.

La chaîne SID peut également prendre la forme « &lt; sid = S-x-x-xx-XXXXXXXXXX-XXXXXXXXXX-xxxxxxxx-xxx &gt; », où la partie « S-X-x-xx-XXXXXXXXXX-XXXXXXXXXX-xxxxxxxx-xxx » est identique à la chaîne retournée par la fonction [**ConvertSidToStringSid a**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .

Lors de la liaison à l’aide du SID de l’objet, certaines méthodes et propriétés [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) ne sont pas prises en charge. Les propriétés **IADs** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du SID de l’objet :

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nom**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Les méthodes **IADsContainer** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du SID de l’objet :

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Créés**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Supprimer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Pour utiliser ces méthodes et propriétés après avoir effectué une liaison à un objet à l’aide du SID d’objet, utilisez la méthode [**IADs. obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le nom unique de l’objet, puis utilisez le nom unique pour effectuer une nouvelle liaison à l’objet.

L’exemple de code suivant montre comment convertir un **objectSID** en chaîne pouvant être liée.


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



 

 