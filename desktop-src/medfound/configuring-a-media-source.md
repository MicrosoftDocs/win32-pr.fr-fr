---
description: Configuration d’une source de média
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configuration d’une source de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e6737d643db2ee473214586cd7ded4f9596133dac5f4fb177df4d7b6b19757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880590"
---
# <a name="configuring-a-media-source"></a>Configuration d’une source de média

Lorsque vous utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média, vous pouvez spécifier une banque de propriétés qui contient les propriétés de configuration. Ces propriétés sont utilisées pour initialiser la source du média. L’ensemble des propriétés prises en charge dépend de l’implémentation de la source du média. Toutes les sources de média ne définissent pas les propriétés de configuration.

Le tableau suivant répertorie les propriétés de configuration des sources de média fournies dans Media Foundation. Les sources de média tierces peuvent définir leurs propres propriétés personnalisées.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Source du média</th>
<th>Propriétés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Source réseau</td>
<td>Voir <a href="network-source-features.md">fonctionnalités de la source réseau</a>.</td>
</tr>
<tr class="even">
<td>Source de média ASF</td>
<td><ul>
<li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li>
<li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Pour configurer une source, procédez comme suit.

1.  Appelez **PSCreateMemoryPropertyStore** pour créer une banque de propriétés. Cette fonction retourne un pointeur **IPropertyStore** .
2.  Appelez **IPropertyStore :: SetValue** pour définir une ou plusieurs propriétés de configuration.
3.  Appelez l’une des fonctions de création du programme de résolution source, telles que [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), et transmettez le pointeur **IPropertyStore** dans le paramètre *pProps* .


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Le programme de résolution source transmet directement le pointeur **IPropertyStore** au gestionnaire de schéma ou au gestionnaire de flux d’octets qui crée la source. Le programme de résolution source n’effectue aucune tentative de validation des propriétés.

En règle générale, ces propriétés sont utilisées pour les paramètres avancés. Si vous ne fournissez pas de banque de propriétés, la source du média doit toujours fonctionner correctement avec les paramètres par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 



