---
title: Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP
description: Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, négociation de format vidéo
- Plug-ins DSP, négociation de format vidéo
- plug-ins vidéo DSP, négociation de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310165"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP

Avant que le lecteur Windows Media insère un plug-in de DSP vidéo dans la chaîne de signal, le joueur doit déterminer si le plug-in peut traiter la vidéo en cours de lecture. Le processus par lequel le plug-in et le lecteur communiquent à propos des formats vidéo pris en charge est appelé négociation de format.

## <a name="providing-the-supported-input-and-output-types"></a>Fournir les types d’entrée et de sortie pris en charge

Si le plug-in DSP agit comme un objet multimédia DirectX (DMO), le lecteur interroge le plug-in sur ses formats pris en charge en effectuant une séquence d’appels à **IMediaObject :: GetInputType** et **IMediaObject :: GetOutputType**.

Si le plug-in DSP agit en tant que Media Foundation Transform (MFT), le lecteur interroge le plug-in sur ses formats pris en charge en effectuant une séquence d’appels à **IMFTransform :: GetInputAvailableType** et **IMFTransform :: GetOutputAvailableType**.

L’exemple de plug-in vidéo généré par l’Assistant de plug-in du lecteur Windows Media stocke la liste des formats vidéo pris en charge sous la forme d’un tableau de GUID. Le code suivant provient du fichier main. cpp :


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



Le lecteur peut appeler **IMediaObject :: GetInputType** et **IMediaObject :: GetOutputType** dans n’importe quel ordre, de sorte que le code de plug-in doit anticiper cela. De même, le lecteur peut appeler **IMFTransform :: GetInputAvailableType** et **IMFTransform :: GetOutputAvailableType** dans n’importe quel ordre. Les exemples d’implémentation de **GetOutputType** et **GetOutputAvailableType** testent si le type d’entrée a déjà été défini. Si c’est le cas, le plug-in répond qu’il ne prend en charge que ce type. Dans le cas contraire, le plug-in retourne le type qui correspond à l’index fourni, comme le montre le code suivant :


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>Définition des types d’entrée et de sortie

Si le plug-in DSP agit comme DMO, le lecteur Windows Media définit le type de média en appelant **IMediaObject :: SetInputType** et **IMediaObject :: SetOutputType**, en transmettant à chaque fonction un pointeur vers une structure de **\_ \_ type de média DMO** qui représente le type de média demandé.

Si le plug-in DSP agit en tant que MFT, le lecteur Windows Media définit le type de média en appelant **IMFTransform :: SetInputType** et **IMFTransform :: SetOutputType**, en passant à chaque fonction un pointeur vers une interface **IMFMediaType** qui représente le type de média demandé.

Il n’y a aucune garantie que le lecteur appellera les méthodes de négociation de format dans un ordre particulier, de sorte que le code de plug-in doit gérer tous les cas. Par exemple, si le lecteur appelle **SetOutputType** avant d’appeler **SetInputType**, il s’agit d’un cours d’action valide pour que le plug-in rejette le type de média de sortie proposé. Le code suivant de l’exemple d’implémentation de **IMediaObject :: SetOutputType** illustre ce qui suit :


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



Les exemples d’implémentations de plug-in de **SetInputType** et **SetOutputType** appellent la fonction personnalisée nommée **ValidateMediaType**. Cette fonction de plug-in effectue une série de tests sur le type de média proposé, conçu pour garantir que le type de média est correctement construit et pris en charge par le plug-in. **ValidateMediaType** effectue les tests suivants :

-   Vérifie que les membres **MajorType** et **formatType** contiennent les valeurs correctes.
-   Vérifie que le membre de **sous-type** correspond à l’un des formats pris en charge.
-   Vérifie que les informations contenues dans les structures **BITMAPINFOHEADER** et **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** contiennent des valeurs valides.
-   Teste si les types de média d’entrée et de sortie correspondent parce que le plug-in ne convertit pas les formats de l’entrée en sortie.

Si le type de média proposé passe les tests de validation, il est stocké dans une variable membre : **m \_ mtInput** pour le type de média d’entrée, **m \_ mtOutput** pour le type de média de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in de DSP vidéo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




