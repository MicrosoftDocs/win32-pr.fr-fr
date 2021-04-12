---
description: Cette rubrique explique comment créer et inscrire des gestionnaires de propriétés pour utiliser le système de propriétés Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisation des gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203098"
---
# <a name="initializing-property-handlers"></a>Initialisation des gestionnaires de propriétés

Cette rubrique explique comment créer et inscrire des gestionnaires de propriétés pour utiliser le système de propriétés Windows.

Cette rubrique est organisée comme suit :

-   [Gestionnaires de propriétés](#property-handlers)
-   [Avant de commencer](#before-you-begin)
-   [Initialisation des gestionnaires de propriétés](#initializing-property-handlers)
-   [Banque de propriétés en mémoire](#in-memory-property-store)
-   [Gestion des valeurs de PROPVARIANT-Based](#dealing-with-propvariant-based-values)
-   [Prise en charge des métadonnées ouvertes](#supporting-open-metadata)
-   [Contenu de texte intégral](#full-text-contents)
-   [Fournir des valeurs pour les propriétés](#providing-values-for-properties)
-   [Écriture des valeurs de retour](#writing-back-values)
-   [Implémentation de IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Inscription et distribution des gestionnaires de propriétés](#registering-and-distributing-property-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="property-handlers"></a>Gestionnaires de propriétés

Les gestionnaires de propriétés constituent une partie essentielle du système de propriétés. Elles sont appelées in-process par l’indexeur pour lire et indexer les valeurs de propriété, et elles sont également appelées par l’Explorateur Windows en mode in-process pour lire et écrire des valeurs de propriété directement dans les fichiers. Ces gestionnaires doivent être écrits et testés avec soin pour éviter la dégradation des performances ou la perte de données dans les fichiers affectés. Pour plus d’informations sur les considérations spécifiques à l’indexeur qui affectent l’implémentation du gestionnaire de propriétés, consultez [développement de gestionnaires de propriétés pour Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

Cette rubrique présente un exemple de format de fichier basé sur XML qui décrit une recette avec une extension de nom de fichier. recipe. L’extension de nom de fichier. Recipe est inscrite en tant que format de fichier distinct plutôt que de s’appuyer sur le format de fichier. Xml plus générique, dont le gestionnaire utilise un flux secondaire pour stocker les propriétés. Nous vous recommandons d’inscrire des extensions de nom de fichier uniques pour vos types de fichiers.

## <a name="before-you-begin"></a>Avant de commencer

Les gestionnaires de propriétés sont des objets COM qui créent l’abstraction [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour un format de fichier spécifique. Ils lisent (analysent) et écrivent ce format de fichier d’une manière conforme à sa spécification. Certains gestionnaires de propriétés effectuent leur travail en fonction d’API qui extraient l’accès à un format de fichier spécifique. Avant de développer un gestionnaire de propriétés pour votre format de fichier, vous devez comprendre comment votre format de fichier stocke les propriétés et comment ces propriétés (noms et valeurs) sont mappées à l’abstraction de la Banque de propriétés.

Quand vous planifiez votre implémentation, n’oubliez pas que les gestionnaires de propriétés sont des composants de bas niveau qui sont chargés dans le contexte de processus tels que l’Explorateur Windows, l’indexeur de recherche Windows et des applications tierces qui utilisent le modèle de programmation d’élément de Shell. Par conséquent, les gestionnaires de propriétés ne peuvent pas être implémentés en code managé et doivent être implémentés en C++. Si votre gestionnaire utilise des API ou des services pour effectuer son travail, vous devez vous assurer que ces services peuvent fonctionner correctement dans le ou les environnements dans lesquels votre gestionnaire de propriétés est chargé.

> [!Note]  
> Les gestionnaires de propriétés sont toujours associés à des types de fichiers spécifiques ; ainsi, si votre format de fichier contient des propriétés qui nécessitent un gestionnaire de propriétés personnalisées, vous devez toujours inscrire une extension de nom de fichier unique pour chaque format de fichier.

 

## <a name="initializing-property-handlers"></a>Initialisation des gestionnaires de propriétés

Avant qu’une propriété ne soit utilisée par le système, elle est initialisée en appelant une implémentation d' [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). Le gestionnaire de propriétés doit être initialisé en faisant en sorte que le système lui affecte un flux au lieu de quitter cette assignation à l’implémentation du gestionnaire. Cette méthode d’initialisation garantit les éléments suivants :

-   Le gestionnaire de propriétés peut s’exécuter dans un processus restreint (une fonctionnalité de sécurité importante) sans disposer de droits d’accès pour lire ou écrire directement des fichiers, plutôt que d’accéder à leur contenu via le flux.
-   Le système peut être approuvé pour gérer correctement les oplocks de fichiers, ce qui constitue une mesure de fiabilité importante.
-   Le système de propriétés fournit un service d’enregistrement sécurisé automatique sans aucune fonctionnalité supplémentaire requise à partir de l’implémentation du gestionnaire de propriétés. Pour plus d’informations sur les flux, consultez la section [écriture des valeurs de retour](#writing-back-values) .
-   L’utilisation de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) fait abstraction de votre implémentation des détails du système de fichiers. Cela permet au gestionnaire de prendre en charge l’initialisation par le biais de stockages alternatifs tels qu’un dossier protocole FTP (FTP) ou un fichier compressé avec une extension de nom de fichier. zip.

Dans certains cas, l’initialisation avec des flux n’est pas possible. Dans ce cas, il existe deux autres interfaces que les gestionnaires de propriétés peuvent implémenter : [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) et [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Si un gestionnaire de propriétés n’implémente pas l' [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), il doit choisir de ne pas s’exécuter dans le processus isolé dans lequel l’indexeur système le placerait par défaut en cas de modification du flux. Pour désactiver cette fonctionnalité, définissez la valeur de Registre suivante.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Toutefois, il est nettement préférable d’implémenter [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) et d’effectuer une initialisation basée sur un flux. Votre gestionnaire de propriétés sera plus sûr et plus fiable en conséquence. La désactivation de l’isolation de processus est généralement prévue uniquement pour les gestionnaires de propriétés hérités et doit être évitée de manière ardue par tout nouveau code.

Pour examiner en détail l’implémentation d’un gestionnaire de propriétés, examinez l’exemple de code suivant, qui est une implémentation de [**IInitializeWithStream :: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). Le gestionnaire est initialisé en chargeant un document de recette XML à l’aide d’un pointeur vers l’instance [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associée à ce document. La variable **\_ spDocEle** utilisée près de la fin de l’exemple de code est définie plus tôt dans l’exemple en tant que msxml2 :: IXMLDOMElementPtr.

> [!Note]  
> Les exemples de code suivants et suivants sont extraits de l’exemple de gestionnaire de recette inclus dans le kit de développement logiciel (SDK) Windows. .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

Une fois le document lui-même chargé, les propriétés à afficher dans l’Explorateur Windows sont chargées en appelant la méthode protégée **\_ LoadProperties** , comme illustré dans l’exemple de code suivant. Ce processus est examiné en détail dans la section suivante.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Si le flux est en lecture seule mais que le paramètre *grfMode* contient l' \_ indicateur STGM ReadWrite, l’initialisation doit échouer et retourner STG \_ E \_ ACCESSDENIED. Sans cette vérification, l’Explorateur Windows affiche les valeurs de propriété comme étant accessibles en écriture, même si ce n’est pas le cas, ce qui complique l’expérience de l’utilisateur final.

Le gestionnaire de propriétés n’est initialisé qu’une seule fois pendant sa durée de vie. Si une deuxième initialisation est demandée, le gestionnaire doit retourner `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>Banque de propriétés de In-Memory

Avant d’examiner l’implémentation de **\_ LoadProperties**, vous devez comprendre le tableau **PropertyMap** utilisé dans l’exemple pour mapper les propriétés du document XML aux propriétés existantes dans le système de propriétés par le biais de leurs valeurs de groupe de propriétés.

Vous ne devez pas exposer tous les éléments et attributs du fichier XML en tant que propriété. Au lieu de cela, sélectionnez uniquement celles que vous jugerez utiles pour les utilisateurs finaux de l’organisation de leurs documents (dans ce cas, recettes). Il s’agit d’un concept important à prendre en compte lors du développement de vos gestionnaires de propriétés : la différence entre les informations réellement utiles pour les scénarios organisationnels et les informations qui appartiennent aux détails de votre fichier et qui peuvent être consultées en ouvrant le fichier lui-même. Les propriétés ne sont pas destinées à être une duplication complète d’un fichier XML.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Voici l’implémentation complète de la méthode **\_ LoadProperties** appelée par [**IInitializeWithStream :: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



La méthode **\_ LoadProperties** appelle la fonction d’assistance de Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés en mémoire (cache) pour les propriétés gérées. À l’aide d’un cache, les modifications sont suivies pour vous. Cela vous évite de suivre si une valeur de propriété a été modifiée dans le cache, mais pas encore enregistrée dans un stockage persistant. Elle vous évite également d’avoir à conserver inutilement des valeurs de propriété qui n’ont pas changé.

La méthode **\_ LoadProperties** appelle également **\_ LoadProperty** , dont l’implémentation est illustrée dans le code suivant) une fois pour chaque propriété mappée. **\_ LoadProperty** obtient la valeur de la propriété telle qu’elle est spécifiée dans l’élément **PropertyMap** du flux XML et l’assigne au cache en mémoire via un appel à [**IPropertyStoreCache :: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). L' \_ indicateur normal PSC dans l’appel à **IPropertyStoreCache :: SetValueAndState** indique que la valeur de propriété n’a pas été modifiée depuis l’entrée dans le cache.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Gestion des valeurs de PROPVARIANT-Based

Dans l’implémentation de **\_ LoadProperty**, une valeur de propriété est fournie sous la forme d’un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Un ensemble d’API dans le kit de développement logiciel (SDK) est fourni pour la conversion de types primitifs tels que **PWSTR** ou **int** vers ou à partir de types **PROPVARIANT** . Ces API se trouvent dans Propvarutil. h.

Par exemple, pour convertir un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en chaîne, vous pouvez utiliser [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) , comme illustré ici.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Pour initialiser un PROPVARIANT à partir d’une chaîne, vous pouvez utiliser [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Comme vous pouvez le voir dans l’un des fichiers de recette inclus dans l’exemple, il peut y avoir plus d’un mot clé dans chaque fichier. Pour tenir compte de cela, le système de propriétés prend en charge les chaînes à valeurs multiples représentées sous forme de vecteur de chaînes (par exemple, « VT \_ Vector \| VT \_ LPWStr »). La méthode **\_ LoadVectorProperty** dans l’exemple utilise des valeurs vectorielles.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Si une valeur n’existe pas dans le fichier, ne retourne pas d’erreur. Au lieu de cela, définissez la valeur sur VT \_ vide et retournez **S \_ OK**. VT \_ vide indique que la valeur de propriété n’existe pas.

## <a name="supporting-open-metadata"></a>Prise en charge des métadonnées ouvertes

Cet exemple utilise un format de fichier basé sur XML. Son schéma peut être étendu pour prendre en charge des propriétés qui n’ont pas été considérées pendant la developmet, par exemple. Ce système est connu sous le nom de métadonnées ouvertes. Cet exemple étend le système de propriétés en créant un nœud sous l’élément **Recipe** appelé **ExtendedProperties**, comme illustré dans l’exemple de code suivant.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Pour charger des propriétés étendues persistantes pendant l’initialisation, implémentez la méthode **\_ LoadExtendedProperties** , comme illustré dans l’exemple de code suivant.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



Les API de sérialisation déclarées dans propsys. h sont utilisées pour sérialiser et désérialiser des types [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en objets BLOB de données, puis l’encodage Base64 est utilisé pour sérialiser ces objets BLOB dans des chaînes qui peuvent être enregistrées dans le fichier XML. Ces chaînes sont stockées dans l’attribut **EncodedValue** de l’élément **ExtendedProperties** . La méthode utilitaire suivante, implémentée dans le fichier util. cpp de l’exemple, effectue la sérialisation. Elle commence par un appel à la fonction [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) pour effectuer la sérialisation binaire, comme illustré dans l’exemple de code suivant.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Ensuite, la fonction [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â, déclarée dans wincrypt. h, effectue la conversion en base64.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



La fonction **DeserializePropVariantFromString** , également trouvée dans util. cpp, inverse l’opération et désérialise les valeurs à partir du fichier XML.

Pour plus d’informations sur la prise en charge des métadonnées ouvertes, consultez « types de fichiers prenant en charge les métadonnées ouvertes » dans [types de fichiers](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Contenu de Full-Text

Les gestionnaires de propriétés peuvent également faciliter une recherche en texte intégral sur le contenu du fichier, et constituent un moyen simple de fournir cette fonctionnalité si le format de fichier n’est pas trop complexe. Il existe une méthode alternative plus puissante pour fournir le texte intégral du fichier par le biais de l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

Le tableau suivant récapitule les avantages de chaque approche à l’aide d' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).



| Fonctionnalité                                   | Filtres                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| Autorise l’écriture différée dans les fichiers ?                  | Non                           | Oui            |
| Fournit une combinaison de contenu et de propriétés ?      | Oui                          | Oui            |
| Multilingue?                                | Oui                          | Non             |
| MIME/Embedded ?                               | Oui                          | Non             |
| Limites du texte ?                             | Phrase, paragraphe, chapitre | Aucun           |
| Implémentation prise en charge pour SPS/SQL Server ? | Oui                          | Non             |
| Implémentation                               | Complex                      | Simple         |



 

Dans l’exemple de gestionnaire de recette, le format de fichier de recette n’a pas d’exigences complexes, donc seul [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a été implémenté pour la prise en charge de la recherche en texte intégral. La recherche en texte intégral est implémentée pour les nœuds XML nommés dans le tableau suivant.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



Le système de propriétés contient la `System.Search.Contents` propriété (contenu de recherche de groupe de \_ \_ caractères), créée pour fournir le contenu de texte intégral à l’indexeur. La valeur de cette propriété n’est jamais affichée directement dans l’interface utilisateur ; le texte de tous les nœuds XML nommés dans le tableau ci-dessus est concaténé dans une chaîne unique. Cette chaîne est ensuite fournie à l’indexeur en tant que contenu de texte intégral du fichier de recette via un appel à [**IPropertyStoreCache :: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , comme illustré dans l’exemple de code suivant.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Fournir des valeurs pour les propriétés

Lorsqu’ils sont utilisés pour lire des valeurs, les gestionnaires de propriétés sont généralement appelés pour l’une des raisons suivantes :

-   Pour énumérer toutes les valeurs de propriété.
-   Pour obtenir la valeur d’une propriété spécifique.

Pour l’énumération, un gestionnaire de propriétés est invité à énumérer ses propriétés lors de l’indexation ou lorsque la boîte de dialogue Propriétés demande l’affichage des propriétés dans l' **autre** groupe. L’indexation s’effectue constamment en tant qu’opération en arrière-plan. Chaque fois qu’un fichier est modifié, l’indexeur est notifié et réindexe le fichier en demandant au gestionnaire de propriétés d’énumérer ses propriétés. Par conséquent, il est essentiel que les gestionnaires de propriétés soient implémentés efficacement et retournent des valeurs de propriété aussi rapidement que possible. Énumérez toutes les propriétés pour lesquelles vous avez des valeurs, comme vous le feriez pour n’importe quelle collection, mais n’énumérez pas les propriétés qui impliquent des calculs gourmands en mémoire ou des demandes réseau qui pourraient les rendre plus lentes à récupérer.

Lors de l’écriture d’un gestionnaire de propriétés, vous devez généralement prendre en compte les deux ensembles de propriétés suivants.

-   Propriétés principales : propriétés que votre type de fichier prend en charge en mode natif. Par exemple, un gestionnaire de propriétés de photos pour les métadonnées EXIF (Exchangeable Image File) prend en charge en mode natif `System.Photo.FNumber` .
-   Propriétés étendues : propriétés que votre type de fichier prend en charge dans le cadre des métadonnées ouvertes.

Étant donné que l’exemple utilise le cache en mémoire, l’implémentation des méthodes [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) est simplement une question de délégation à ce cache, comme illustré dans l’exemple de code suivant.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Si vous choisissez de ne pas déléguer au cache en mémoire, vous devez implémenter vos méthodes pour fournir> le comportement attendu suivant :

-   [**IPropertyStore :: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): s’il n’existe aucune propriété, cette méthode retourne **S \_ OK**.
-   [**IPropertyStore :: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): si *iProp* est supérieur ou égal à *CProps*, cette méthode retourne E \_ INVALIDARG et la structure vers laquelle pointe le paramètre *de* la ligne de base est remplie avec des zéros.
-   [**IPropertyStore :: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) et [**IPropertyStore :: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflètent l’état actuel du gestionnaire de propriétés. Si une [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) est ajoutée ou supprimée du fichier via [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), ces deux méthodes doivent refléter cette modification la prochaine fois qu’elles sont appelées.
-   [**IPropertyStore :: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): si cette méthode est demandée pour une valeur qui n’existe pas, elle retourne **S \_ OK** avec la valeur signalée comme VT \_ vide.

## <a name="writing-back-values"></a>Écriture des valeurs de retour

Quand le gestionnaire de propriétés écrit la valeur d’une propriété à l’aide de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), il n’écrit pas la valeur dans le fichier tant que [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) n’est pas appelé. Le cache en mémoire peut être utile pour implémenter ce schéma. Dans l’exemple de code, l’implémentation de **IPropertyStore :: SetValue** définit simplement la nouvelle valeur dans le cache en mémoire et définit l’état de cette propriété sur PSC \_ Dirty.


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



Dans toute implémentation de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , le comportement suivant est attendu de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Si la propriété existe déjà, la valeur de la propriété est définie.
-   Si la propriété n’existe pas, la nouvelle propriété est ajoutée et sa valeur est définie.
-   Si la valeur de propriété ne peut pas être rendue persistante à la même précision que celle donnée (par exemple, la troncation en raison de limitations de taille dans le format de fichier), la valeur est définie autant que possible et les inplaces \_ \_ tronquées sont retournées.
-   Si la propriété n’est pas prise en charge par le gestionnaire de propriétés, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` est retourné.
-   S’il existe une autre raison pour laquelle la valeur de la propriété ne peut pas être définie, comme le fichier verrouillé ou le manque de droits à modifier via les listes de contrôle d’accès (ACL), STG \_ E \_ ACCESSDENIED est retourné.

L’un des principaux avantages de l’utilisation de flux, comme l’exemple, est la fiabilité. Les gestionnaires de propriétés doivent toujours considérer qu’ils ne peuvent pas conserver un fichier dans un état incohérent dans le cas d’une défaillance catastrophique. L’endommagement des fichiers d’un utilisateur est évidemment évité, et la meilleure façon de le faire est d’utiliser un mécanisme de « copie sur écriture ». Si votre gestionnaire de propriétés utilise un flux pour accéder à un fichier, vous recevez ce comportement automatiquement. le système écrit toutes les modifications apportées au flux, en remplaçant le fichier par la nouvelle copie uniquement pendant l’opération de validation.

Pour remplacer ce comportement et contrôler manuellement le processus d’enregistrement du fichier, vous pouvez désactiver le comportement d’enregistrement sécurisé en définissant la valeur ManualSafeSave dans l’entrée de registre de votre gestionnaire, comme illustré ici.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Lorsqu’un gestionnaire spécifie la valeur ManualSafeSave, le flux avec lequel il est initialisé n’est pas un flux traité (STGM \_ traité). Le gestionnaire lui-même doit implémenter la fonction Safe Save pour s’assurer que le fichier n’est pas endommagé si l’opération d’enregistrement est interrompue. Si le gestionnaire implémente l’écriture sur place, il écrit dans le flux de données qu’il reçoit. Si le gestionnaire ne prend pas en charge cette fonctionnalité, il doit récupérer un flux avec lequel écrire la copie mise à jour du fichier à l’aide de [**IDestinationStreamFactory :: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Une fois l’écriture terminée, le gestionnaire doit appeler [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) sur le flux d’origine pour terminer l’opération et remplacer le contenu du flux d’origine par la nouvelle copie du fichier.

ManualSafeSave est également la situation par défaut si vous n’initialisez pas votre gestionnaire avec un flux. Sans un flux d’origine pour recevoir le contenu du flux temporaire, vous devez utiliser [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) pour effectuer un remplacement atomique du fichier source.

Les formats de fichiers volumineux qui seront utilisés de manière à produire des fichiers de plus de 1 Mo doivent implémenter la prise en charge de l’écriture de propriété sur place ; dans le cas contraire, le comportement des performances ne répond pas aux attentes des clients du système de propriétés. Dans ce scénario, la durée nécessaire à l’écriture des propriétés ne doit pas être affectée par la taille du fichier.

Pour les fichiers de très grande taille, par exemple un fichier vidéo de 1 Go ou plus, une autre solution est requise. S’il n’y a pas assez d’espace dans le fichier pour effectuer une écriture sur place, le gestionnaire peut échouer à la mise à jour de propriété si la quantité d’espace réservée à l’écriture de propriété sur place est épuisée. Cet échec se produit pour éviter des performances médiocres dues à 2 Go d’e/s (1 à lire, 1 à écrire). En raison de cette défaillance potentielle, ces formats de fichier doivent réserver suffisamment d’espace pour l’écriture de propriété sur place.

Si le fichier a suffisamment d’espace dans son en-tête pour écrire des métadonnées, et si l’écriture de ces métadonnées n’entraîne pas l’augmentation ou la réduction du fichier, l’écriture sur place peut être sécurisée. Nous vous recommandons 64 Ko comme point de départ. L’écriture sur place équivaut au gestionnaire qui demande ManualSafeSave et appelle [**IStream :: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) dans l’implémentation de [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), et offre de bien meilleures performances que la copie en écriture. Si la taille du fichier change en raison des modifications apportées à la valeur de la propriété, l’écriture sur place ne doit pas être tentée en raison du risque de corruption d’un fichier dans le cas d’un arrêt anormal.

> [!Note]  
> Pour des raisons de performances, nous vous recommandons d’utiliser l’option ManualSafeSave avec les gestionnaires de propriétés qui utilisent des fichiers de 100 Ko ou plus.

 

Comme illustré dans l’exemple d’implémentation suivant de [**IPropertyStore :: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), le gestionnaire de ManualSafeSave est inscrit pour illustrer l’option d’enregistrement sécurisé manuel. La méthode **\_ SaveCacheToDom** écrit les valeurs de propriété stockées dans le cache en mémoire dans l’objet XMLdocument.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



Ensuite, demandez si pécifiée prend en charge [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



Ensuite, validez le flux d’origine, qui écrit les données dans le fichier d’origine de manière sûre.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



Examinez ensuite l’implémentation de **\_ SaveCacheToDom** .


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Ensuite, récupérez le nombre de propriétés stockées dans le cache en mémoire.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



À présent, itérez au sein des propriétés pour déterminer si la valeur d’une propriété a été modifiée depuis son chargement en mémoire.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



La méthode [**IPropertyStoreCache :: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) obtient l’état de la propriété dans le cache. L’indicateur de modification du PSC \_ , qui a été défini dans l’implémentation de [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marque une propriété comme modifiée.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Mappez la propriété au nœud XML comme spécifié dans le tableau **exemple \_ rgPropertyMap** .


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Si une propriété ne figure pas dans le mappage, il s’agit d’une nouvelle propriété qui a été définie par l’Explorateur Windows. Étant donné que les métadonnées ouvertes sont prises en charge, enregistrez la nouvelle propriété dans la section **ExtendedProperties** du document XML.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Implémentation de IPropertyStoreCapabilities

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informe l’interface utilisateur de l’interpréteur de commandes si une propriété particulière peut être modifiée dans l’interface utilisateur de l’interpréteur de commandes. Il est important de noter que cela concerne uniquement la possibilité de modifier la propriété dans l’interface utilisateur, pas si vous pouvez appeler [**IPropertyStore :: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) sur la propriété. Une propriété qui provoque une valeur de retour de S \_ false à partir de [**IPropertyStoreCapabilities :: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) peut toujours être capable d’être définie par le biais d’une application.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) retourne **S \_ OK** pour indiquer que les utilisateurs finaux doivent être autorisés à modifier la propriété directement ; S \_ false indique qu’elles ne doivent pas. S \_ false peut signifier que les applications sont responsables de l’écriture de la propriété, et non des utilisateurs. L’interpréteur de commandes désactive les contrôles d’édition selon les besoins en fonction des résultats des appels à cette méthode. Un gestionnaire qui n’implémente pas [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) est supposé prendre en charge les métadonnées ouvertes via la prise en charge de l’écriture d’une propriété.

Si vous générez un gestionnaire qui gère uniquement les propriétés en lecture seule, vous devez implémenter votre méthode **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) afin qu’il retourne STG \_ E ACCESSDENIED lorsqu’il est \_ appelé avec l' \_ indicateur STGM ReadWrite.

L’attribut [isInnate](./propdesc-schema-typeinfo.md) de certaines propriétés est défini sur **true**. Les propriétés innées présentent les caractéristiques suivantes :

-   La propriété est généralement calculée d’une certaine façon. Par exemple, `System.Image.BitDepth` est calculé à partir de l’image elle-même.
-   La modification de la propriété n’a pas de sens sans modifier le fichier. Par exemple, la modification de `System.Image.Dimensions` l’image ne peut pas être redimensionnée, donc il n’est pas judicieux d’autoriser l’utilisateur à la modifier.
-   Dans certains cas, ces propriétés sont fournies automatiquement par le système. Les exemples incluent `System.DateModified` , qui est fourni par le système de fichiers, et `System.SharedWith` , qui est basé sur la personne avec laquelle l’utilisateur partage le fichier.

En raison de ces caractéristiques, les propriétés marquées comme *IsInnate* sont fournies à l’utilisateur dans l’interface utilisateur du shell uniquement en tant que propriétés en lecture seule. Si une propriété est marquée comme *IsInnate*, le système de propriétés ne stocke pas cette propriété dans le gestionnaire de propriétés. Par conséquent, les gestionnaires de propriétés n’ont pas besoin de code spécial pour prendre en compte ces propriétés dans leurs implémentations. Si la valeur de l’attribut *IsInnate* n’est pas explicitement indiquée pour une propriété particulière, la valeur par défaut est **false**.

## <a name="registering-and-distributing-property-handlers"></a>Inscription et distribution des gestionnaires de propriétés

Avec le gestionnaire de propriétés implémenté, il doit être enregistré et son extension de nom de fichier associée au gestionnaire. Pour plus d’informations, consultez [inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnement des gestionnaires de propriétés](./building-property-handlers-properties.md)
</dt> <dt>

[Utilisation des noms de genres](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Utilisation des listes de propriétés](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md)
</dt> <dt>

[Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
