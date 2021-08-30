---
title: Comment énumérer les polices
description: Cette vue d’ensemble indique comment énumérer les polices de la collection de polices système, par nom de famille.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6823ef48a596ffff941f61135a42f53f9dc351edd51f16325afb6288f85ac136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048939"
---
# <a name="how-to-enumerate-fonts"></a>Comment énumérer les polices

Cette vue d’ensemble indique comment énumérer les polices de la collection de polices système, par nom de famille.

Cette vue d’ensemble se compose des éléments suivants :

-   [Étape 1 : obtenir la collection de polices système.](#step-1-get-the-system-font-collection)
-   [Étape 2 : obtenir le nombre de familles de polices.](#step-2-get-the-font-family-count)
-   [Créer une boucle for.](#make-a-for-loop)
    -   [Étape 3 : obtenir la famille de polices.](#step-3-get-the-font-family)
    -   [Étape 4 : obtenir les noms de famille.](#step-4-get-the-family-names)
    -   [Étape 5 : Rechercher le nom des paramètres régionaux.](#step-5-find-the-locale-name)
    -   [Étape 6 : obtenir la longueur de la chaîne de nom de famille et la chaîne.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Conclusion](#conclusion)
-   [Exemple de code](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Étape 1 : obtenir la collection de polices système.

utilisez la méthode [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fournie par la fabrique DirectWrite pour retourner un [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) avec toutes les polices système qu’il contient.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Étape 2 : obtenir le nombre de familles de polices.

Ensuite, récupérez le nombre de familles de polices à partir de la collection de polices à l’aide de [**IDWriteFontCollection :: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). Nous allons l’utiliser pour effectuer une boucle sur chaque famille de polices de la collection.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Créer une boucle for.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Maintenant que vous disposez de la collection de polices et du nombre de polices, les étapes restantes sont en boucle sur chaque famille de polices, récupérant l’objet [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) et interrogeant celui-ci.

### <a name="step-3-get-the-font-family"></a>Étape 3 : obtenir la famille de polices.

Obtenir un objet [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) à l’aide de [**IDWriteFontCollection :: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) et en lui passant l’index actuel, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Étape 4 : obtenir les noms de famille.

Récupérez les noms des familles de polices à l’aide de [**IDWriteFontFamily :: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Il s’agit d’un objet [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) . Il peut avoir plusieurs versions localisées du nom de famille pour la famille de polices.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Étape 5 : Rechercher le nom des paramètres régionaux.

Récupérez le nom de la police famliy dans les paramètres régionaux de votre choix à l’aide de la méthode [**IDWriteLocalizedStrings :: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) . Dans ce cas, les paramètres régionaux par défaut sont d’abord récupérés et demandés. Si cela ne fonctionne pas, les paramètres régionaux « en-US » sont demandés. Si l’un des paramètres régionaux spécifiés est introuvable, cet exemple revient simplement à l’index 0, les premiers paramètres régionaux disponibles.


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Étape 6 : obtenir la longueur de la chaîne de nom de famille et la chaîne.

Enfin, récupérez la longueur de la chaîne de nom de famille à l’aide de [**IDWriteLocalizedStrings :: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Utilisez cette longueur pour allouer une chaîne suffisamment grande pour contenir le nom, puis obtenir le nom de famille de polices à l’aide de [**IDWriteLocalizedStrings :: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a>Conclusion

Une fois que vous avez le ou les noms de famille dans les paramètres régionaux, vous pouvez les répertorier pour permettre à l’utilisateur de choisir ou de le passer à CreateTextFormat pour commencer la mise en forme du texte avec la famille de polices spécifiée, et ainsi de suite.

## <a name="example-code"></a>Exemple de code

Pour voir le code source complet de cet exemple, consultez l' [exemple d’énumération font](/samples/browse/?redirectedfrom=MSDN-samples).

 

 