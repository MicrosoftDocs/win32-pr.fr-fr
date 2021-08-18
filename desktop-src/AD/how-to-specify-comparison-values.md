---
title: Comment spécifier des valeurs de comparaison
description: Chaque type d’attribut a une syntaxe qui détermine le type de valeurs de comparaison que vous pouvez spécifier dans un filtre de recherche pour cet attribut.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Comment spécifier des valeurs de comparaison AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5babc7d9781895c9671594214e4e036a85ef951cdb4b97ba34d708d160dd8fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188120"
---
# <a name="how-to-specify-comparison-values"></a>Comment spécifier des valeurs de comparaison

Chaque type d’attribut a une syntaxe qui détermine le type de valeurs de comparaison que vous pouvez spécifier dans un filtre de recherche pour cet attribut.

Les sections suivantes décrivent les conditions requises pour chaque syntaxe d’attribut. Pour plus d’informations sur les syntaxes d’attribut, consultez [syntaxes pour les attributs dans Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Expression
</dt> <dd>

La valeur spécifiée dans un filtre doit être une valeur de chaîne « TRUE » ou « FALSe ». Les exemples suivants montrent comment spécifier une chaîne de comparaison booléenne.

L’exemple suivant recherche les objets dont le **showInAdvancedViewOnly** est défini sur **true**:


```C++
(showInAdvancedViewOnly=TRUE)
```



L’exemple suivant recherche les objets dont le **showInAdvancedViewOnly** est défini sur **false**:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Entier et énumération
</dt> <dd>

La valeur spécifiée dans un filtre doit être un entier décimal. Les valeurs hexadécimales doivent être converties au format décimal. Une chaîne de comparaison de valeurs prend la forme suivante :


```C++
<attribute name>:<value>
```



" <attribute name> " est le **lDAPDisplayName** de l’attribut et "<value>"est la valeur à utiliser pour la comparaison.

L’exemple de code suivant affiche un filtre qui recherche les objets dont la valeur de **GroupType** est égale à l’indicateur de groupe **\_ \_ \_ universel de \_ type** de groupe ADS (8) et l’indicateur de **\_ sécurité de type de groupe \_ \_ \_ ADS** (0x80000000). Les deux indicateurs combinés égal à 0x80000008, qui sont convertis en décimal est 2147483656.


```C++
(groupType=2147483656)
```



Les opérateurs de règle de correspondance LDAP peuvent également être utilisés pour effectuer des comparaisons au niveau du bit. Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax). L’exemple de code suivant affiche un filtre qui recherche les objets qui ont un **GroupType** avec le bit de **\_ type de groupe ADS \_ \_ Security \_ Enabled** (0x80000000 = 2147483648) défini.


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

La valeur spécifiée dans un filtre correspond aux données à trouver. Les données doivent être représentées sous la forme d’une chaîne d’octets encodée en deux caractères, où chaque octet est précédé d’une barre oblique inverse ( \\ ). Par exemple, la valeur 0x05 apparaît dans la chaîne sous la forme « \\ 05 ».

La fonction [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) peut être utilisée pour créer une représentation sous forme de chaîne encodée de données binaires. La fonction **ADsEncodeBinaryData** ne code pas les valeurs d’octets qui représentent des caractères alphanumériques. Au lieu de cela, il placera le caractère dans la chaîne sans l’encoder. Cela entraîne la chaîne contenant un mélange de caractères encodés et non codés. Par exemple, si les données binaires sont 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32, la chaîne encodée contient « \\ 05 \\ 1a \\ 1BC2 ». Cela n’a aucun effet sur le filtre et les filtres de recherche fonctionnent correctement avec ces types de chaînes.

Les caractères génériques sont acceptés.

L’exemple de code suivant montre un filtre qui contient la chaîne encodée pour **schemaIDGUID** avec la valeur Guid « {BF967ABA-0DE6-11D0-A285-00AA003049E2} » :


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid
</dt> <dd>

La valeur spécifiée dans un filtre est la représentation sous forme de chaîne d’octets encodée du SID. Pour plus d’informations sur les chaînes d’octets encodées, consultez la section précédente de cette rubrique, qui traite de la syntaxe OctetString.

L’exemple de code suivant montre un filtre qui contient une chaîne encodée pour **objectSID** avec la valeur de chaîne sid « S-1-5-21-1935655697-308236825-1417001333 » :


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>UNIQUES
</dt> <dd>

Le nom unique complet, à mettre en correspondance, doit être fourni.

Les caractères génériques ne sont pas acceptés.

Sachez que l’attribut **objectCategory** vous permet également de spécifier le **lDAPDisplayName** de la classe définie sur l’attribut.

L’exemple suivant montre un filtre qui spécifie un **membre** qui contient "CN = TESTUSER, DC = fabrikam, DC = com" :


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

La valeur spécifiée dans un filtre doit être un entier décimal. Convertit les valeurs hexadécimales en décimal.

L’exemple de code suivant montre un filtre qui spécifie un **CreationTime** défini sur un [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de « 1999-12-31 23:59:59 (UTC/GMT) » :


```C++
(creationTime=125911583990000000)
```



Les fonctions suivantes créent un filtre match (=) exact pour un attribut entier volumineux et vérifient l’attribut dans le schéma et sa syntaxe :


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString
</dt> <dd>

Les attributs avec ces syntaxes doivent adhérer à des jeux de caractères spécifiques. Pour plus d’informations, consultez [syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Actuellement, les Active Directory Domain Services n’appliquent pas ces jeux de caractères.

La valeur spécifiée dans un filtre est une chaîne. La comparaison respecte la casse.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

La valeur spécifiée dans un filtre est une chaîne qui représente la date sous la forme suivante :


```C++
YYYYMMDDHHMMSS.0Z
```



« 0Z » indique qu’il n’y a pas de différence de temps. N’oubliez pas que le serveur Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time). Si un différentiel de temps n’est pas spécifié, la valeur par défaut est GMT.

Si le fuseau horaire local n’est pas GMT, utilisez une valeur différentielle pour spécifier votre fuseau horaire local et appliquer l’différentielle à l’heure GMT. La différence est basée sur : GMT = local + différentiel.

Pour spécifier une valeur différentielle, utilisez :


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



L’exemple suivant montre un filtre qui spécifie une durée de **whenCreated** définie à 3/23/99 8:52:58 GMT :


```C++
(whenCreated=19990323205258.0Z)
```



L’exemple suivant montre un filtre qui spécifie une durée de **whenCreated** définie à 3/23/99 8:52:58 pm heure d’hiver Nouvelle-Zélande (différentielle est + 12 heures) :


```C++
(whenCreated=19990323205258.0+1200)
```



L’exemple de code suivant montre comment calculer la différence de fuseau horaire. La fonction retourne l’écart entre le fuseau horaire local actuel et l’heure GMT. La valeur retournée est une chaîne au format suivant :


```C++
[+/-]HHMM
```



Par exemple, l’heure du Pacifique est-0800.


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime
</dt> <dd>

La valeur spécifiée dans un filtre est une chaîne qui représente la date sous la forme suivante :


```C++
YYMMDDHHMMSSZ
```



Z indique qu’il n’y a pas de différence de temps. N’oubliez pas que le serveur Active Directory stocke la date et l’heure sur l’heure GMT. Si un différentiel de temps n’est pas spécifié, la valeur par défaut est GMT.

La valeur de secondes (« SS ») est facultative.

Si l’heure GMT n’est pas le fuseau horaire local, appliquez une valeur différentielle locale pour spécifier votre fuseau horaire local. L’écart est : GMT = local + différentiel.

Pour spécifier une variable différentielle, utilisez la forme suivante :


```C++
YYMMDDHHMMSS[+/-]HHMM
```



L’exemple suivant montre un filtre qui spécifie une durée de **myTimeAttrib** définie à 3/23/99 8:52:58 GMT :


```C++
(myTimeAttrib=990323205258Z)
```



L’exemple suivant montre un filtre qui spécifie une durée **myTimeAttrib** définie à 3/23/99 8:52:58 PM sans secondes spécifiée :


```C++
(myTimeAttrib=9903232052Z)
```



L’exemple suivant montre un filtre qui spécifie une durée de **myTimeAttrib** définie à 3/23/99 8:52:58 pm heure d’hiver Nouvelle-Zélande (différentielle est 12 heures). Cela équivaut à 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

La valeur spécifiée dans un filtre est une chaîne. DirectoryString peut contenir des caractères Unicode. La comparaison respecte la casse.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

L’OID entier à mettre en correspondance doit être fourni.

Les caractères génériques ne sont pas acceptés.

L’attribut **objectCategory** vous permet de spécifier le **lDAPDisplayName** de la classe définie pour l’attribut.

L’exemple suivant montre un filtre qui spécifie **governsID** pour la classe de volume :


```C++
(governsID=1.2.840.113556.1.5.36)
```



Deux filtres équivalents qui spécifient l’attribut **systemMustContain** contenant **uncname**, qui a un OID de 1.2.840.113556.1.4.137 :


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Autres syntaxes
</dt> <dd>

Les syntaxes suivantes sont évaluées dans un filtre semblable à une chaîne d’octets :

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 