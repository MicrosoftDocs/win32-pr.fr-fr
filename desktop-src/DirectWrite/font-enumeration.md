---
title: Comment énumérer les polices
description: Cette vue d’ensemble indique comment énumérer les polices de la collection de polices système, par nom de famille.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382243"
---
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="237d0-103">Comment énumérer les polices</span><span class="sxs-lookup"><span data-stu-id="237d0-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="237d0-104">Cette vue d’ensemble indique comment énumérer les polices de la collection de polices système, par nom de famille.</span><span class="sxs-lookup"><span data-stu-id="237d0-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="237d0-105">Cette vue d’ensemble se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="237d0-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="237d0-106">Étape 1 : obtenir la collection de polices système.</span><span class="sxs-lookup"><span data-stu-id="237d0-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="237d0-107">Étape 2 : obtenir le nombre de familles de polices.</span><span class="sxs-lookup"><span data-stu-id="237d0-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="237d0-108">Créer une boucle for.</span><span class="sxs-lookup"><span data-stu-id="237d0-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="237d0-109">Étape 3 : obtenir la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="237d0-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="237d0-110">Étape 4 : obtenir les noms de famille.</span><span class="sxs-lookup"><span data-stu-id="237d0-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="237d0-111">Étape 5 : Rechercher le nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="237d0-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="237d0-112">Étape 6 : obtenir la longueur de la chaîne de nom de famille et la chaîne.</span><span class="sxs-lookup"><span data-stu-id="237d0-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="237d0-113">Conclusion</span><span class="sxs-lookup"><span data-stu-id="237d0-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="237d0-114">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="237d0-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="237d0-115">Étape 1 : obtenir la collection de polices système.</span><span class="sxs-lookup"><span data-stu-id="237d0-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="237d0-116">Utilisez la méthode [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fournie par la fabrique DirectWrite pour retourner un [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) avec toutes les polices système qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="237d0-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="237d0-117">Étape 2 : obtenir le nombre de familles de polices.</span><span class="sxs-lookup"><span data-stu-id="237d0-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="237d0-118">Ensuite, récupérez le nombre de familles de polices à partir de la collection de polices à l’aide de [**IDWriteFontCollection :: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span><span class="sxs-lookup"><span data-stu-id="237d0-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="237d0-119">Nous allons l’utiliser pour effectuer une boucle sur chaque famille de polices de la collection.</span><span class="sxs-lookup"><span data-stu-id="237d0-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="237d0-120">Créer une boucle for.</span><span class="sxs-lookup"><span data-stu-id="237d0-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="237d0-121">Maintenant que vous disposez de la collection de polices et du nombre de polices, les étapes restantes sont en boucle sur chaque famille de polices, récupérant l’objet [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) et interrogeant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="237d0-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="237d0-122">Étape 3 : obtenir la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="237d0-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="237d0-123">Obtenir un objet [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) à l’aide de [**IDWriteFontCollection :: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) et en lui passant l’index actuel, *i*.</span><span class="sxs-lookup"><span data-stu-id="237d0-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="237d0-124">Étape 4 : obtenir les noms de famille.</span><span class="sxs-lookup"><span data-stu-id="237d0-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="237d0-125">Récupérez les noms des familles de polices à l’aide de [**IDWriteFontFamily :: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="237d0-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="237d0-126">Il s’agit d’un objet [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) .</span><span class="sxs-lookup"><span data-stu-id="237d0-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="237d0-127">Il peut avoir plusieurs versions localisées du nom de famille pour la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="237d0-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="237d0-128">Étape 5 : Rechercher le nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="237d0-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="237d0-129">Récupérez le nom de la police famliy dans les paramètres régionaux de votre choix à l’aide de la méthode [**IDWriteLocalizedStrings :: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) .</span><span class="sxs-lookup"><span data-stu-id="237d0-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="237d0-130">Dans ce cas, les paramètres régionaux par défaut sont d’abord récupérés et demandés.</span><span class="sxs-lookup"><span data-stu-id="237d0-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="237d0-131">Si cela ne fonctionne pas, les paramètres régionaux « en-US » sont demandés.</span><span class="sxs-lookup"><span data-stu-id="237d0-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="237d0-132">Si l’un des paramètres régionaux spécifiés est introuvable, cet exemple revient simplement à l’index 0, les premiers paramètres régionaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="237d0-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="237d0-133">Étape 6 : obtenir la longueur de la chaîne de nom de famille et la chaîne.</span><span class="sxs-lookup"><span data-stu-id="237d0-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="237d0-134">Enfin, récupérez la longueur de la chaîne de nom de famille à l’aide de [**IDWriteLocalizedStrings :: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="237d0-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="237d0-135">Utilisez cette longueur pour allouer une chaîne suffisamment grande pour contenir le nom, puis obtenir le nom de famille de polices à l’aide de [**IDWriteLocalizedStrings :: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span><span class="sxs-lookup"><span data-stu-id="237d0-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="237d0-136">Conclusion</span><span class="sxs-lookup"><span data-stu-id="237d0-136">Conclusion</span></span>

<span data-ttu-id="237d0-137">Une fois que vous avez le ou les noms de famille dans les paramètres régionaux, vous pouvez les répertorier pour permettre à l’utilisateur de choisir ou de le passer à CreateTextFormat pour commencer la mise en forme du texte avec la famille de polices spécifiée, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="237d0-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="237d0-138">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="237d0-138">Example Code</span></span>

<span data-ttu-id="237d0-139">Pour voir le code source complet de cet exemple, consultez l' [exemple d’énumération font](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="237d0-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 