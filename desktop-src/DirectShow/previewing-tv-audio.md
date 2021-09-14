---
description: Aperçu de l’audio TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Aperçu de l’audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223169"
---
# <a name="previewing-tv-audio"></a>Aperçu de l’audio TV

Pour prévisualiser l’audio TV, acheminez le code confidentiel du décodeur audio sur le filtre de la barre transversale vers le code confidentiel du tuner audio. Pour désactiver le son, acheminez le code confidentiel du décodeur audio à-1, comme indiqué dans le diagramme suivant. (Les filtres de distributeur sont décrits dans [utilisation des](working-with-crossbars.md)FlowFilters.)

![routage du code confidentiel du décodeur audio](images/vidcap07.png)

L’approche de base est la suivante :

1.  Utilisez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour localiser le filtre de barre.
2.  Utilisez la méthode [**IAMCrossbar :: obten \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) pour énumérer les broches d’entrée et de sortie du filtre de la barre transversale. Recherchez une broche de sortie décodeur audio et une broche d’entrée de syntoniseur audio.
3.  Si vous trouvez les bons pin, appelez [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) pour acheminer les broches. Si ce n’est pas le cas, recherchez en amont un autre distributeur et répétez le processus.
4.  Pour désactiver le son, acheminez le code confidentiel du décodeur audio à-1.

La plupart des tuners TV utilisent un seul filtre de distributeur, mais certains utilisent deux filtres de distributeur. Par conséquent, vous devrez peut-être Rechercher un deuxième distributeur si le premier échoue.

> [!Note]  
> Contrairement à ce que vous pourriez espérer, aucun filtre de capture audio ou rendu audio n’est requis pour prévisualiser l’audio, car il existe une connexion physique entre la carte tuner et la carte son.

 

Le code suivant illustre ces étapes plus en détail. Tout d’abord, voici une fonction d’assistance qui recherche un type de code confidentiel spécifié dans un filtre de barre.


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



La fonction Next tente d’activer ou de désactiver l’audio, en fonction de la valeur du paramètre *bActivate* . Il recherche les codes confidentiels requis dans le filtre de la barre de filtres spécifié. S’il ne peut pas les trouver, il retourne un code d’erreur.


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



La fonction Next recherche un filtre de barre dans le graphique de filtre. S’il en trouve un, il tente d’activer ou de désactiver le son (à l’aide de la fonction précédente). Si cette opération échoue, la méthode effectue une recherche dans le flux de données pour un deuxième distributeur et tente à nouveau. Pour une approche plus généralisée de la gestion de plusieurs filtres de distributeur dans un graphique, consultez la classe CCrossbar dans l’exemple d’application AmCap.


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



Le code suivant montre comment appeler ces fonctions :


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Notez que ces exemples de fonctions répètent un grand nombre des appels de fonction. Par exemple, ils énumèrent les codes confidentiels du distributeur à chaque fois. Dans une application réelle, vous pouvez mettre en cache certaines de ces informations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Télévision analogique audio](analog-television-audio.md)
</dt> <dt>

[Utilisation des conversions](working-with-crossbars.md)
</dt> </dl>

 

 



