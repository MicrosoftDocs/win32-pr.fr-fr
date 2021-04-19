---
description: Utilisation des chaînes de texte de DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Utilisation des chaînes de texte de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518986"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="71b99-103">Utilisation des chaînes de texte de DVD</span><span class="sxs-lookup"><span data-stu-id="71b99-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="71b99-104">Certains disques DVD, en particulier les disques de karaoké, peuvent contenir une liste de chaînes de texte pour compléter le contenu vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="71b99-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="71b99-105">Ces chaînes de texte contiennent des métadonnées relatives au contenu, telles que les titres des chansons, les noms des artistes, les informations de genre, etc.</span><span class="sxs-lookup"><span data-stu-id="71b99-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="71b99-106">Les chaînes de texte peuvent être présentes dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="71b99-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="71b99-107">Ces chaînes sont facultatives, et de nombreux disques n’en ont pas.</span><span class="sxs-lookup"><span data-stu-id="71b99-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="71b99-108">Pour récupérer des chaînes de texte à partir d’un DVD, utilisez l’interface [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , qui est exposée par le [navigateur DVD](dvd-navigator-filter.md).</span><span class="sxs-lookup"><span data-stu-id="71b99-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="71b99-109">Vous n’avez pas besoin de créer un graphique de lecture DVD pour récupérer les chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="71b99-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="71b99-110">Vous pouvez simplement créer le navigateur DVD, définir le volume DVD, puis appeler les méthodes de chaîne de texte appropriées :</span><span class="sxs-lookup"><span data-stu-id="71b99-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="71b99-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="71b99-111">Method</span></span>                                                                                  | <span data-ttu-id="71b99-112">Description</span><span class="sxs-lookup"><span data-stu-id="71b99-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71b99-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="71b99-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="71b99-114">Obtient le nombre de langues pour lesquelles il existe des chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="71b99-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="71b99-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span><span class="sxs-lookup"><span data-stu-id="71b99-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="71b99-116">Obtient des informations sur les chaînes de texte d’une langue.</span><span class="sxs-lookup"><span data-stu-id="71b99-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="71b99-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span><span class="sxs-lookup"><span data-stu-id="71b99-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="71b99-118">Obtient une chaîne de texte pour une langue spécifiée, par index.</span><span class="sxs-lookup"><span data-stu-id="71b99-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="71b99-119">**IDvdInfo2::GetDVDTextStringAsNative**</span><span class="sxs-lookup"><span data-stu-id="71b99-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="71b99-120">Obtient une chaîne de texte sous la forme d’un tableau d’octets bruts.</span><span class="sxs-lookup"><span data-stu-id="71b99-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="71b99-121">Utilisez cette méthode si la chaîne de texte utilise un encodage de caractères non pris en charge par [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span><span class="sxs-lookup"><span data-stu-id="71b99-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="71b99-122">Voici la procédure de base pour obtenir des chaînes de texte :</span><span class="sxs-lookup"><span data-stu-id="71b99-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="71b99-123">Appelez [**IDvdInfo2 :: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) pour rechercher le nombre total de langues dans lesquelles les chaînes de texte s’affichent.</span><span class="sxs-lookup"><span data-stu-id="71b99-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="71b99-124">Si le nombre est égal à zéro, cela signifie que le DVD n’a pas de chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="71b99-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="71b99-125">(Il s’agit peut-être du cas le plus courant, en fait.)</span><span class="sxs-lookup"><span data-stu-id="71b99-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="71b99-126">Si le nombre de langues est d’au moins un, appelez [**IDvdInfo2 :: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) pour obtenir des informations sur chaque langue.</span><span class="sxs-lookup"><span data-stu-id="71b99-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="71b99-127">La langue est spécifiée par index.</span><span class="sxs-lookup"><span data-stu-id="71b99-127">The language is specified by index.</span></span> <span data-ttu-id="71b99-128">La méthode retourne le nombre total de chaînes de texte dans cette langue, l’identificateur de paramètres régionaux (**LCID**) de la langue et l’encodage de caractères (Unicode ou autre).</span><span class="sxs-lookup"><span data-stu-id="71b99-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="71b99-129">Les chaînes de texte de DVD peuvent utiliser plusieurs jeux de caractères différents ; celles-ci sont répertoriées dans l' [**\_ énumération TextCharSet DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span><span class="sxs-lookup"><span data-stu-id="71b99-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="71b99-130">Pour obtenir une chaîne de texte, appelez [**IDvdInfo2 :: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) ou [**IDvdInfo2 :: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span><span class="sxs-lookup"><span data-stu-id="71b99-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="71b99-131">La première méthode retourne une chaîne de caractères larges, mais ne prend pas en charge tous les jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="71b99-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="71b99-132">La deuxième méthode retourne un tableau d’octets contenant les données de texte brut.</span><span class="sxs-lookup"><span data-stu-id="71b99-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="71b99-133">Pour les deux méthodes, vous pouvez appeler la méthode avec un pointeur de mémoire tampon **null** pour rechercher la taille de la chaîne et le type de texte.</span><span class="sxs-lookup"><span data-stu-id="71b99-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="71b99-134">Allouez ensuite une mémoire tampon et rappelez la méthode pour obtenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="71b99-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="71b99-135">Chaque chaîne de texte est associée à un code d’identificateur qui indique la signification de la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="71b99-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="71b99-136">L’identificateur est retourné en tant que [**valeur \_ TextStringType DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) .</span><span class="sxs-lookup"><span data-stu-id="71b99-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="71b99-137">Il existe deux catégories d’identificateur : les identificateurs de *structure* et les *identificateurs de contenu*.</span><span class="sxs-lookup"><span data-stu-id="71b99-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="71b99-138">Les identificateurs de structure ont des codes numériques dans la plage 0x00 – 0x02F.</span><span class="sxs-lookup"><span data-stu-id="71b99-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="71b99-139">Les identificateurs de contenu ont une plage de 0x30 et supérieure.</span><span class="sxs-lookup"><span data-stu-id="71b99-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="71b99-140">(L’énumération **\_ TextStringType de DVD** définit un sous-ensemble des identificateurs les plus courants, mais les méthodes [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) peuvent retourner tout code d’identificateur.) Un identificateur de structure décrit une partie logique du DVD, telle qu’un volume, un titre ou une partie du titre (PTT).</span><span class="sxs-lookup"><span data-stu-id="71b99-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="71b99-141">Un identificateur de contenu indique la signification d’une chaîne de texte particulière, telle que le titre du film, le titre de la chanson ou le genre.</span><span class="sxs-lookup"><span data-stu-id="71b99-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="71b99-142">Les identificateurs de structure n’ont pas de chaînes de texte associées.</span><span class="sxs-lookup"><span data-stu-id="71b99-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="71b99-143">Lorsqu’un identificateur de structure apparaît dans les données de chaîne de texte, il signale que les chaînes de texte suivantes s’appliquent à cette portion logique du DVD, jusqu’à l’identificateur de structure suivant.</span><span class="sxs-lookup"><span data-stu-id="71b99-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="71b99-144">La position des identificateurs de structure dans les données de texte correspond à la hiérarchie logique du volume DVD.</span><span class="sxs-lookup"><span data-stu-id="71b99-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="71b99-145">Par exemple, la première occurrence de l' \_ identificateur du titre du struct DVD \_ (0x02) représente le premier titre du volume, et l’occurrence suivante représente le deuxième titre.</span><span class="sxs-lookup"><span data-stu-id="71b99-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="71b99-146">Le tableau suivant montre comment les chaînes de texte peuvent être définies pour un DVD avec deux titres.</span><span class="sxs-lookup"><span data-stu-id="71b99-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="71b99-147">\_TEXTSTRINGTYPE DVD</span><span class="sxs-lookup"><span data-stu-id="71b99-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="71b99-148">Chaîne de texte</span><span class="sxs-lookup"><span data-stu-id="71b99-148">Text string</span></span>  | <span data-ttu-id="71b99-149">Description</span><span class="sxs-lookup"><span data-stu-id="71b99-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="71b99-150">\_ \_ Volume de struct DVD (0x01)</span><span class="sxs-lookup"><span data-stu-id="71b99-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="71b99-151">""</span><span class="sxs-lookup"><span data-stu-id="71b99-151">""</span></span>           | <span data-ttu-id="71b99-152">Identificateur de structure pour le côté de l’ensemble du disque.</span><span class="sxs-lookup"><span data-stu-id="71b99-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="71b99-153">\_Nom général du DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="71b99-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="71b99-154">« Volume DVD »</span><span class="sxs-lookup"><span data-stu-id="71b99-154">"DVD Volume"</span></span> | <span data-ttu-id="71b99-155">Nom du volume DVD.</span><span class="sxs-lookup"><span data-stu-id="71b99-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="71b99-156">\_Titre du struct DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="71b99-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="71b99-157">""</span><span class="sxs-lookup"><span data-stu-id="71b99-157">""</span></span>           | <span data-ttu-id="71b99-158">Identificateur de structure pour le premier titre.</span><span class="sxs-lookup"><span data-stu-id="71b99-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="71b99-159">\_Nom général du DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="71b99-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="71b99-160">« Titre 1 »</span><span class="sxs-lookup"><span data-stu-id="71b99-160">"Title 1"</span></span>    | <span data-ttu-id="71b99-161">Nom du premier titre.</span><span class="sxs-lookup"><span data-stu-id="71b99-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="71b99-162">\_Titre du struct DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="71b99-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="71b99-163">""</span><span class="sxs-lookup"><span data-stu-id="71b99-163">""</span></span>           | <span data-ttu-id="71b99-164">Identificateur de structure pour le deuxième titre.</span><span class="sxs-lookup"><span data-stu-id="71b99-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="71b99-165">\_Nom général du DVD \_ (0x30)</span><span class="sxs-lookup"><span data-stu-id="71b99-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="71b99-166">« Titre 2 »</span><span class="sxs-lookup"><span data-stu-id="71b99-166">"Title 2"</span></span>    | <span data-ttu-id="71b99-167">Nom du deuxième titre.</span><span class="sxs-lookup"><span data-stu-id="71b99-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="71b99-168">Les méthodes [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) et [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) traitent les identificateurs de structure et les identificateurs de contenu de la même façon.</span><span class="sxs-lookup"><span data-stu-id="71b99-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="71b99-169">La seule différence est que pour les identificateurs de structure, la mémoire tampon de texte associée est vide.</span><span class="sxs-lookup"><span data-stu-id="71b99-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="71b99-170">C’est à l’application d’effectuer le suivi de la relation entre les chaînes de texte et les portions logiques du DVD.</span><span class="sxs-lookup"><span data-stu-id="71b99-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="71b99-171">L’exemple suivant montre comment obtenir des chaînes de texte à partir d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="71b99-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="71b99-172">Cet exemple ignore certains détails nécessaires à une application réelle.</span><span class="sxs-lookup"><span data-stu-id="71b99-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="71b99-173">(Par exemple, il ignore les identificateurs de structure.) L’exemple est destiné uniquement à illustrer la séquence correcte des appels.</span><span class="sxs-lookup"><span data-stu-id="71b99-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="71b99-174">Pour plus d’informations sur les chaînes de texte de DVD, consultez le [site Web du Forum DVD](https://go.microsoft.com/fwlink/?LinkId=8677).</span><span class="sxs-lookup"><span data-stu-id="71b99-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="71b99-175">La méthode **CDvdCore :: GetDvdText** de l’application DVDSample montre les étapes de base de l’énumération et de l’affichage des chaînes de texte de DVD.</span><span class="sxs-lookup"><span data-stu-id="71b99-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71b99-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71b99-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b99-177">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="71b99-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



