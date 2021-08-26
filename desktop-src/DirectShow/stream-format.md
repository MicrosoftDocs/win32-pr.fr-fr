---
description: Format de flux
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Format de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ed1ac4501a2d8f081c12fef75baf15aaebd442fc182a116db1038c2a73523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903989"
---
# <a name="stream-format"></a>Format de flux

Les pilotes MSDV et UVC peuvent tous les deux générer deux formats DV : audio entrelacé, vidéo ou vidéo entrelacé. Audio entrelacé-vidéo est le format d’origine de l’appareil. Le format vidéo uniquement contient les mêmes données, mais les exemples sont marqués comme n’ayant pas de données audio. Le format vidéo uniquement existe principalement pour la compatibilité avec les applications qui utilisent la vidéo pour Windows. Pour plus d’informations, consultez [type-1 et fichiers AVI DV](type-1-vs--type-2-dv-avi-files.md)type-2.

**Pilote MSDV**

Le pilote MSDV a deux broches de sortie. La première broche de sortie envoie des données entrelacées, et la deuxième broche de sortie envoie des données vidéo uniquement. Une seule broche de sortie peut être connectée à la fois. Pour sélectionner un format, connectez la broche de sortie appropriée. Vous pouvez utiliser l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sur la broche de sortie pour rechercher le format.

**Pilote UVC**

Contrairement au pilote MSDV, le pilote UVC remet les deux formats du même code PIN. Le format par défaut est vidéo uniquement. Pour sélectionner le format, utilisez l’interface **IAMStreamConfig** sur la broche de sortie. Appelez la méthode **GetStreamCaps** pour énumérer les types de média sur la broche de sortie. Pour chaque type de média, si le type principal correspond au format souhaité, appelez **SetFormat** et transmettez ce type de média.



| Format                      | Type principal             |
|-----------------------------|------------------------|
| Audio et vidéo entrelacés | MEDIATYPE \_ entrelacé |
| Vidéo uniquement                  | Vidéo de MEDIATYPE \_       |



 

La fonction suivante définit le format en fonction du GUID du type principal.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



Le pilote MSDV prend également en charge **IAMStreamConfig**. vous pouvez donc écrire du code qui fonctionne pour les deux types d’appareils.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



