---
description: Utilisation des chaînes de texte de DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Utilisation des chaînes de texte de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238757"
---
# <a name="working-with-dvd-text-strings"></a>Utilisation des chaînes de texte de DVD

Certains disques DVD, en particulier les disques de karaoké, peuvent contenir une liste de chaînes de texte pour compléter le contenu vidéo ou audio. Ces chaînes de texte contiennent des métadonnées relatives au contenu, telles que les titres des chansons, les noms des artistes, les informations de genre, etc. Les chaînes de texte peuvent être présentes dans plusieurs langues. Ces chaînes sont facultatives, et de nombreux disques n’en ont pas.

Pour récupérer des chaînes de texte à partir d’un DVD, utilisez l’interface [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , qui est exposée par le [navigateur DVD](dvd-navigator-filter.md). Vous n’avez pas besoin de créer un graphique de lecture DVD pour récupérer les chaînes de texte. Vous pouvez simplement créer le navigateur DVD, définir le volume DVD, puis appeler les méthodes de chaîne de texte appropriées :



| Méthode                                                                                  | Description                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Obtient le nombre de langues pour lesquelles il existe des chaînes de texte.                                                                                                                                  |
| [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Obtient des informations sur les chaînes de texte d’une langue.                                                                                                                                       |
| [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Obtient une chaîne de texte pour une langue spécifiée, par index.                                                                                                                                          |
| [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Obtient une chaîne de texte sous la forme d’un tableau d’octets bruts. Utilisez cette méthode si la chaîne de texte utilise un encodage de caractères non pris en charge par [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode). |



 

Voici la procédure de base pour obtenir des chaînes de texte :

1.  Appelez [**IDvdInfo2 :: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) pour rechercher le nombre total de langues dans lesquelles les chaînes de texte s’affichent. Si le nombre est égal à zéro, cela signifie que le DVD n’a pas de chaînes de texte. (Il s’agit peut-être du cas le plus courant, en fait.)
2.  Si le nombre de langues est d’au moins un, appelez [**IDvdInfo2 :: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) pour obtenir des informations sur chaque langue. La langue est spécifiée par index. La méthode retourne le nombre total de chaînes de texte dans cette langue, l’identificateur de paramètres régionaux (**LCID**) de la langue et l’encodage de caractères (Unicode ou autre). Les chaînes de texte de DVD peuvent utiliser plusieurs jeux de caractères différents ; celles-ci sont répertoriées dans l' [**\_ énumération TextCharSet DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).
3.  Pour obtenir une chaîne de texte, appelez [**IDvdInfo2 :: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) ou [**IDvdInfo2 :: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative). La première méthode retourne une chaîne de caractères larges, mais ne prend pas en charge tous les jeux de caractères. La deuxième méthode retourne un tableau d’octets contenant les données de texte brut. Pour les deux méthodes, vous pouvez appeler la méthode avec un pointeur de mémoire tampon **null** pour rechercher la taille de la chaîne et le type de texte. Allouez ensuite une mémoire tampon et rappelez la méthode pour obtenir la chaîne.

Chaque chaîne de texte est associée à un code d’identificateur qui indique la signification de la chaîne de texte. L’identificateur est retourné en tant que [**valeur \_ TextStringType DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) . Il existe deux catégories d’identificateur : les identificateurs de *structure* et les *identificateurs de contenu*. Les identificateurs de structure ont des codes numériques dans la plage 0x00 – 0x02F. Les identificateurs de contenu ont une plage de 0x30 et supérieure. (L’énumération **\_ TextStringType de DVD** définit un sous-ensemble des identificateurs les plus courants, mais les méthodes [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) peuvent retourner tout code d’identificateur.) Un identificateur de structure décrit une partie logique du DVD, telle qu’un volume, un titre ou une partie du titre (PTT). Un identificateur de contenu indique la signification d’une chaîne de texte particulière, telle que le titre du film, le titre de la chanson ou le genre.

Les identificateurs de structure n’ont pas de chaînes de texte associées. Lorsqu’un identificateur de structure apparaît dans les données de chaîne de texte, il signale que les chaînes de texte suivantes s’appliquent à cette portion logique du DVD, jusqu’à l’identificateur de structure suivant. La position des identificateurs de structure dans les données de texte correspond à la hiérarchie logique du volume DVD. Par exemple, la première occurrence de l' \_ identificateur du titre du struct DVD \_ (0x02) représente le premier titre du volume, et l’occurrence suivante représente le deuxième titre.

Le tableau suivant montre comment les chaînes de texte peuvent être définies pour un DVD avec deux titres.



| \_TEXTSTRINGTYPE DVD        | Chaîne de texte  | Description                                    |
|----------------------------|--------------|------------------------------------------------|
| \_ \_ Volume de struct DVD (0x01) | ""           | Identificateur de structure pour le côté de l’ensemble du disque. |
| \_Nom général du DVD \_ (0x30)  | « Volume DVD » | Nom du volume DVD.                               |
| \_Titre du struct DVD \_ (0x02)  | ""           | Identificateur de structure pour le premier titre.      |
| \_Nom général du DVD \_ (0x30)  | « Titre 1 »    | Nom du premier titre.                       |
| \_Titre du struct DVD \_ (0x02)  | ""           | Identificateur de structure pour le deuxième titre.     |
| \_Nom général du DVD \_ (0x30)  | « Titre 2 »    | Nom du deuxième titre.                      |



 

Les méthodes [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) et [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) traitent les identificateurs de structure et les identificateurs de contenu de la même façon. La seule différence est que pour les identificateurs de structure, la mémoire tampon de texte associée est vide. C’est à l’application d’effectuer le suivi de la relation entre les chaînes de texte et les portions logiques du DVD.

L’exemple suivant montre comment obtenir des chaînes de texte à partir d’un DVD. Cet exemple ignore certains détails nécessaires à une application réelle. (Par exemple, il ignore les identificateurs de structure.) L’exemple est destiné uniquement à illustrer la séquence correcte des appels.


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



Pour plus d’informations sur les chaînes de texte de DVD, consultez le [site Web du Forum DVD](https://go.microsoft.com/fwlink/?LinkId=8677).

La méthode **CDvdCore :: GetDvdText** de l’application DVDSample montre les étapes de base de l’énumération et de l’affichage des chaînes de texte de DVD.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



