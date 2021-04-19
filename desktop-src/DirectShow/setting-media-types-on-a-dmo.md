---
description: Définition des types de médias sur un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Définition des types de médias sur un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523109"
---
# <a name="setting-media-types-on-a-dmo"></a>Définition des types de médias sur un DMO

Avant qu’un DMO puisse traiter des données, le client doit définir le type de média pour chaque flux. (Il existe une exception mineure pour cette règle ; consultez [flux facultatifs](optional-streams.md).) Pour rechercher le nombre de flux, appelez la méthode [**IMediaObject :: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Cette méthode retourne deux valeurs, le nombre d’entrées et le nombre de sorties. Ces valeurs sont fixes pour la durée de vie de la DMO.

**Types préférés**

Pour chaque flux, DMO attribue une liste de types de média possibles, par ordre de préférence. Par exemple, les types préférés peuvent être 32-RGB, RVB 24 bits et RVB 16 bits, dans cet ordre. Lorsque le client définit les types de médias, il peut utiliser ces listes comme un indicateur. Pour récupérer un type préféré pour un flux, appelez la méthode [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) ou [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) . Spécifiez le numéro du flux et une valeur d’index pour le type (à partir de zéro). Par exemple, le code suivant récupère le premier type préféré dans le premier flux d’entrée :


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Pour énumérer tous les types de médias préférés sur un flux donné, utilisez une boucle qui incrémente l’index de type jusqu’à ce que la méthode retourne DMO \_ E \_ plus d' \_ \_ éléments, comme illustré dans l’exemple suivant :


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Vous devez noter les points suivants sur les types préférés :

-   DMO peut retourner un type qui n’a aucun bloc de format. Par exemple, un DMO peut spécifier un type de vidéo, tel que RVB 24 bits, sans fournir la largeur et la hauteur de l’image. Toutefois, lorsque vous définissez le type, vous devez fournir un bloc de format complet. (Certains types de média, comme MIDI, ne requièrent jamais de bloc de format, auquel cas cette remarque ne s’applique pas.)
-   DMO n’est pas requis pour prendre en charge toutes les combinaisons de types préférés qu’il retourne. Par exemple, si un DMO a deux flux et que chaque flux a quatre types préférés, il existe 16 combinaisons possibles, mais elles ne sont pas toutes garanties comme étant valides.
-   Lorsque le client définit le type de média pour un flux, DMO peut mettre à jour les types préférés pour d’autres flux afin de refléter le nouvel État. Toutefois, cela n’est pas obligatoire.
-   Pour certains flux, DMO peut ne pas proposer de types préférés. En règle générale, un DMO doit offrir au moins certains types préférés sur certains flux.
-   DMO n’est pas obligé d’offrir une liste complète des types de médias qu’il peut accepter. Il peut y avoir des types « non publiés » pris en charge par DMO, mais qui ne sont pas proposés comme types préférés.

En bref, le client doit traiter les types préférés comme des indications uniquement. La seule façon de savoir quels types sont pris en charge consiste à les tester, comme décrit dans la section suivante.

**Définition du type de média sur un flux**

Utilisez les méthodes [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) et [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) pour définir le type de chaque flux. Vous devez fournir une structure de **\_ \_ type de média DMO** qui contient une description complète du type de média. L’exemple suivant définit le type de média sur le flux d’entrée 0, à l’aide de l’audio PCM stéréo 44,1 kHz 16 bits :


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Pour tester un type de média sans le définir, appelez **SetInputType** ou **SetOutputType** avec l' \_ indicateur DMO Set \_ TYPEF \_ test \_ only. La méthode retourne S \_ OK si le type est acceptable, ou a la \_ valeur false dans le cas contraire :


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Étant donné que les paramètres d’un flux peuvent affecter un autre flux, vous devrez peut-être effacer le type de média d’un flux. Pour ce faire, appelez **SetInputType** ou **SetOutputType** avec l' \_ indicateur Set \_ TYPEF \_ Clear de DMO.

Pour un décodeur DMO, le client définit en premier le type d’entrée, puis choisit un type de sortie. Pour un encodeur DMO, le client définit d’abord le type de sortie, puis le type d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



