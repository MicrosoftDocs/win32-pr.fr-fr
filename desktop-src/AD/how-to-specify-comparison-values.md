---
title: Comment spécifier des valeurs de comparaison
description: Chaque type d’attribut a une syntaxe qui détermine le type de valeurs de comparaison que vous pouvez spécifier dans un filtre de recherche pour cet attribut.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Comment spécifier des valeurs de comparaison AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edba238961cdc18b088b6b5bd5b06ff4be383add
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386749"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="f6de1-104">Comment spécifier des valeurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="f6de1-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="f6de1-105">Chaque type d’attribut a une syntaxe qui détermine le type de valeurs de comparaison que vous pouvez spécifier dans un filtre de recherche pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f6de1-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="f6de1-106">Les sections suivantes décrivent les conditions requises pour chaque syntaxe d’attribut.</span><span class="sxs-lookup"><span data-stu-id="f6de1-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="f6de1-107">Pour plus d’informations sur les syntaxes d’attribut, consultez [syntaxes pour les attributs dans Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="f6de1-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="f6de1-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Expression</span><span class="sxs-lookup"><span data-stu-id="f6de1-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-109">La valeur spécifiée dans un filtre doit être une valeur de chaîne « TRUE » ou « FALSe ».</span><span class="sxs-lookup"><span data-stu-id="f6de1-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="f6de1-110">Les exemples suivants montrent comment spécifier une chaîne de comparaison booléenne.</span><span class="sxs-lookup"><span data-stu-id="f6de1-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="f6de1-111">L’exemple suivant recherche les objets dont le **showInAdvancedViewOnly** est défini sur **true**:</span><span class="sxs-lookup"><span data-stu-id="f6de1-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="f6de1-112">L’exemple suivant recherche les objets dont le **showInAdvancedViewOnly** est défini sur **false**:</span><span class="sxs-lookup"><span data-stu-id="f6de1-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="f6de1-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Entier et énumération</span><span class="sxs-lookup"><span data-stu-id="f6de1-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-114">La valeur spécifiée dans un filtre doit être un entier décimal.</span><span class="sxs-lookup"><span data-stu-id="f6de1-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="f6de1-115">Les valeurs hexadécimales doivent être converties au format décimal.</span><span class="sxs-lookup"><span data-stu-id="f6de1-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="f6de1-116">Une chaîne de comparaison de valeurs prend la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f6de1-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="f6de1-117">" <attribute name> " est le **lDAPDisplayName** de l’attribut et "</span><span class="sxs-lookup"><span data-stu-id="f6de1-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="f6de1-118">"est la valeur à utiliser pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="f6de1-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="f6de1-119">L’exemple de code suivant affiche un filtre qui recherche les objets dont la valeur de **GroupType** est égale à l’indicateur de groupe **\_ \_ \_ universel de \_ type** de groupe ADS (8) et l’indicateur de **\_ sécurité de type de groupe \_ \_ \_ ADS** (0x80000000).</span><span class="sxs-lookup"><span data-stu-id="f6de1-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="f6de1-120">Les deux indicateurs combinés égal à 0x80000008, qui sont convertis en décimal est 2147483656.</span><span class="sxs-lookup"><span data-stu-id="f6de1-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="f6de1-121">Les opérateurs de règle de correspondance LDAP peuvent également être utilisés pour effectuer des comparaisons au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="f6de1-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="f6de1-122">Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="f6de1-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="f6de1-123">L’exemple de code suivant affiche un filtre qui recherche les objets qui ont un **GroupType** avec le bit de **\_ type de groupe ADS \_ \_ Security \_ Enabled** (0x80000000 = 2147483648) défini.</span><span class="sxs-lookup"><span data-stu-id="f6de1-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="f6de1-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span><span class="sxs-lookup"><span data-stu-id="f6de1-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-125">La valeur spécifiée dans un filtre correspond aux données à trouver.</span><span class="sxs-lookup"><span data-stu-id="f6de1-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="f6de1-126">Les données doivent être représentées sous la forme d’une chaîne d’octets encodée en deux caractères, où chaque octet est précédé d’une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f6de1-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\\).</span></span> <span data-ttu-id="f6de1-127">Par exemple, la valeur 0x05 apparaît dans la chaîne sous la forme « \\ 05 ».</span><span class="sxs-lookup"><span data-stu-id="f6de1-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="f6de1-128">La fonction [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) peut être utilisée pour créer une représentation sous forme de chaîne encodée de données binaires.</span><span class="sxs-lookup"><span data-stu-id="f6de1-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="f6de1-129">La fonction **ADsEncodeBinaryData** ne code pas les valeurs d’octets qui représentent des caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="f6de1-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="f6de1-130">Au lieu de cela, il placera le caractère dans la chaîne sans l’encoder.</span><span class="sxs-lookup"><span data-stu-id="f6de1-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="f6de1-131">Cela entraîne la chaîne contenant un mélange de caractères encodés et non codés.</span><span class="sxs-lookup"><span data-stu-id="f6de1-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="f6de1-132">Par exemple, si les données binaires sont 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32, la chaîne encodée contient « \\ 05 \\ 1a \\ 1BC2 ».</span><span class="sxs-lookup"><span data-stu-id="f6de1-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="f6de1-133">Cela n’a aucun effet sur le filtre et les filtres de recherche fonctionnent correctement avec ces types de chaînes.</span><span class="sxs-lookup"><span data-stu-id="f6de1-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="f6de1-134">Les caractères génériques sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="f6de1-134">Wildcards are accepted.</span></span>

<span data-ttu-id="f6de1-135">L’exemple de code suivant montre un filtre qui contient la chaîne encodée pour **schemaIDGUID** avec la valeur Guid « {BF967ABA-0DE6-11D0-A285-00AA003049E2} » :</span><span class="sxs-lookup"><span data-stu-id="f6de1-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="f6de1-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span><span class="sxs-lookup"><span data-stu-id="f6de1-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-137">La valeur spécifiée dans un filtre est la représentation sous forme de chaîne d’octets encodée du SID.</span><span class="sxs-lookup"><span data-stu-id="f6de1-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="f6de1-138">Pour plus d’informations sur les chaînes d’octets encodées, consultez la section précédente de cette rubrique, qui traite de la syntaxe OctetString.</span><span class="sxs-lookup"><span data-stu-id="f6de1-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="f6de1-139">L’exemple de code suivant montre un filtre qui contient une chaîne encodée pour **objectSID** avec la valeur de chaîne sid « S-1-5-21-1935655697-308236825-1417001333 » :</span><span class="sxs-lookup"><span data-stu-id="f6de1-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="f6de1-140"><span id="DN"></span><span id="dn"></span>UNIQUES</span><span class="sxs-lookup"><span data-stu-id="f6de1-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-141">Le nom unique complet, à mettre en correspondance, doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="f6de1-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="f6de1-142">Les caractères génériques ne sont pas acceptés.</span><span class="sxs-lookup"><span data-stu-id="f6de1-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="f6de1-143">Sachez que l’attribut **objectCategory** vous permet également de spécifier le **lDAPDisplayName** de la classe définie sur l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f6de1-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="f6de1-144">L’exemple suivant montre un filtre qui spécifie un **membre** qui contient "CN = TESTUSER, DC = fabrikam, DC = com" :</span><span class="sxs-lookup"><span data-stu-id="f6de1-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="f6de1-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="f6de1-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-146">La valeur spécifiée dans un filtre doit être un entier décimal.</span><span class="sxs-lookup"><span data-stu-id="f6de1-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="f6de1-147">Convertit les valeurs hexadécimales en décimal.</span><span class="sxs-lookup"><span data-stu-id="f6de1-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="f6de1-148">L’exemple de code suivant montre un filtre qui spécifie un **CreationTime** défini sur un [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de « 1999-12-31 23:59:59 (UTC/GMT) » :</span><span class="sxs-lookup"><span data-stu-id="f6de1-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="f6de1-149">Les fonctions suivantes créent un filtre match (=) exact pour un attribut entier volumineux et vérifient l’attribut dans le schéma et sa syntaxe :</span><span class="sxs-lookup"><span data-stu-id="f6de1-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


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

<span data-ttu-id="f6de1-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span><span class="sxs-lookup"><span data-stu-id="f6de1-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-151">Les attributs avec ces syntaxes doivent adhérer à des jeux de caractères spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f6de1-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="f6de1-152">Pour plus d’informations, consultez [syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="f6de1-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="f6de1-153">Actuellement, les Active Directory Domain Services n’appliquent pas ces jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="f6de1-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="f6de1-154">La valeur spécifiée dans un filtre est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f6de1-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="f6de1-155">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="f6de1-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="f6de1-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="f6de1-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-157">La valeur spécifiée dans un filtre est une chaîne qui représente la date sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f6de1-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="f6de1-158">« 0Z » indique qu’il n’y a pas de différence de temps.</span><span class="sxs-lookup"><span data-stu-id="f6de1-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="f6de1-159">N’oubliez pas que le serveur Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="f6de1-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="f6de1-160">Si un différentiel de temps n’est pas spécifié, la valeur par défaut est GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="f6de1-161">Si le fuseau horaire local n’est pas GMT, utilisez une valeur différentielle pour spécifier votre fuseau horaire local et appliquer l’différentielle à l’heure GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="f6de1-162">La différence est basée sur : GMT = local + différentiel.</span><span class="sxs-lookup"><span data-stu-id="f6de1-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="f6de1-163">Pour spécifier une valeur différentielle, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f6de1-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="f6de1-164">L’exemple suivant montre un filtre qui spécifie une durée de **whenCreated** définie à 3/23/99 8:52:58 GMT :</span><span class="sxs-lookup"><span data-stu-id="f6de1-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="f6de1-165">L’exemple suivant montre un filtre qui spécifie une durée de **whenCreated** définie à 3/23/99 8:52:58 pm heure d’hiver Nouvelle-Zélande (différentielle est + 12 heures) :</span><span class="sxs-lookup"><span data-stu-id="f6de1-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="f6de1-166">L’exemple de code suivant montre comment calculer la différence de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="f6de1-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="f6de1-167">La fonction retourne l’écart entre le fuseau horaire local actuel et l’heure GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="f6de1-168">La valeur retournée est une chaîne au format suivant :</span><span class="sxs-lookup"><span data-stu-id="f6de1-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="f6de1-169">Par exemple, l’heure du Pacifique est-0800.</span><span class="sxs-lookup"><span data-stu-id="f6de1-169">For example, Pacific Standard Time is -0800.</span></span>


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

<span data-ttu-id="f6de1-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span><span class="sxs-lookup"><span data-stu-id="f6de1-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-171">La valeur spécifiée dans un filtre est une chaîne qui représente la date sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f6de1-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="f6de1-172">Z indique qu’il n’y a pas de différence de temps.</span><span class="sxs-lookup"><span data-stu-id="f6de1-172">Z indicates no time differential.</span></span> <span data-ttu-id="f6de1-173">N’oubliez pas que le serveur Active Directory stocke la date et l’heure sur l’heure GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="f6de1-174">Si un différentiel de temps n’est pas spécifié, la valeur par défaut est GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="f6de1-175">La valeur de secondes (« SS ») est facultative.</span><span class="sxs-lookup"><span data-stu-id="f6de1-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="f6de1-176">Si l’heure GMT n’est pas le fuseau horaire local, appliquez une valeur différentielle locale pour spécifier votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="f6de1-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="f6de1-177">L’écart est : GMT = local + différentiel.</span><span class="sxs-lookup"><span data-stu-id="f6de1-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="f6de1-178">Pour spécifier une variable différentielle, utilisez la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f6de1-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="f6de1-179">L’exemple suivant montre un filtre qui spécifie une durée de **myTimeAttrib** définie à 3/23/99 8:52:58 GMT :</span><span class="sxs-lookup"><span data-stu-id="f6de1-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="f6de1-180">L’exemple suivant montre un filtre qui spécifie une durée **myTimeAttrib** définie à 3/23/99 8:52:58 PM sans secondes spécifiée :</span><span class="sxs-lookup"><span data-stu-id="f6de1-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="f6de1-181">L’exemple suivant montre un filtre qui spécifie une durée de **myTimeAttrib** définie à 3/23/99 8:52:58 pm heure d’hiver Nouvelle-Zélande (différentielle est 12 heures).</span><span class="sxs-lookup"><span data-stu-id="f6de1-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="f6de1-182">Cela équivaut à 3/23/99 8:52:58 AM GMT.</span><span class="sxs-lookup"><span data-stu-id="f6de1-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="f6de1-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span><span class="sxs-lookup"><span data-stu-id="f6de1-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-184">La valeur spécifiée dans un filtre est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f6de1-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="f6de1-185">DirectoryString peut contenir des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6de1-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="f6de1-186">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="f6de1-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="f6de1-187"><span id="OID"></span><span id="oid"></span>OID</span><span class="sxs-lookup"><span data-stu-id="f6de1-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-188">L’OID entier à mettre en correspondance doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="f6de1-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="f6de1-189">Les caractères génériques ne sont pas acceptés.</span><span class="sxs-lookup"><span data-stu-id="f6de1-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="f6de1-190">L’attribut **objectCategory** vous permet de spécifier le **lDAPDisplayName** de la classe définie pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f6de1-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="f6de1-191">L’exemple suivant montre un filtre qui spécifie **governsID** pour la classe de volume :</span><span class="sxs-lookup"><span data-stu-id="f6de1-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="f6de1-192">Deux filtres équivalents qui spécifient l’attribut **systemMustContain** contenant **uncname**, qui a un OID de 1.2.840.113556.1.4.137 :</span><span class="sxs-lookup"><span data-stu-id="f6de1-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="f6de1-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Autres syntaxes</span><span class="sxs-lookup"><span data-stu-id="f6de1-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="f6de1-194">Les syntaxes suivantes sont évaluées dans un filtre semblable à une chaîne d’octets :</span><span class="sxs-lookup"><span data-stu-id="f6de1-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="f6de1-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="f6de1-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="f6de1-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="f6de1-196">AccessPointDN</span></span>
-   <span data-ttu-id="f6de1-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="f6de1-197">PresentationAddresses</span></span>
-   <span data-ttu-id="f6de1-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="f6de1-198">ReplicaLink</span></span>
-   <span data-ttu-id="f6de1-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="f6de1-199">DNWithString</span></span>
-   <span data-ttu-id="f6de1-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="f6de1-200">DNWithOctetString</span></span>
-   <span data-ttu-id="f6de1-201">ORName</span><span class="sxs-lookup"><span data-stu-id="f6de1-201">ORName</span></span>

</dd> </dl>

 

 