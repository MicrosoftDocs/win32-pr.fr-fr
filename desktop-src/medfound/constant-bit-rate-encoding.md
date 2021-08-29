---
description: Encodage à vitesse binaire constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Encodage à vitesse binaire constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318cbf6d1a0b9c635fcd8313589581839fe74c7402411d59a1b5dfbdb55739d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974828"
---
# <a name="constant-bit-rate-encoding"></a>Encodage à vitesse binaire constante

Dans l’encodage CBR (constant bit rate), l’encodeur connaît la vitesse de transmission des échantillons de média de sortie et la fenêtre de mémoire tampon (paramètres de compartiment avec fuite) avant le début de la session de codage. L’encodeur utilise le même nombre de bits pour encoder chaque seconde de l’échantillon tout au long de la durée du fichier pour atteindre la vitesse de transmission cible d’un flux. Cela limite la variation de la taille des exemples de flux. En outre, pendant la session d’encodage, la vitesse de transmission n’est pas exactement à la valeur spécifiée, mais reste proche de la vitesse de transmission cible.

L'encodage en mode CBR est utile quand vous voulez connaître le débit binaire ou la durée approximative d'un fichier sans analyser le fichier complet. Ceci est requis dans les scénarios de diffusion en continu dans lesquels le contenu multimédia doit être diffusé à un débit binaire prévisible et avec une utilisation cohérente de la bande passante.

L’inconvénient de l’encodage CBR est que la qualité du contenu encodé n’est pas constante. Étant donné que le contenu est plus difficile à compresser, les parties d’un flux CBR auront une qualité inférieure à celle des autres. Par exemple, un film classique présente des scènes relativement statiques et des scènes qui sont pleines d’actions. Si vous encodez un film à l’aide de CBR, les scènes qui sont statiques et, par conséquent, faciles à coder efficacement, présentent une qualité supérieure à celle des scènes d’action, ce qui aurait nécessité des tailles d’échantillonnage supérieures pour maintenir la même qualité.

En général, les variations de la qualité d’un fichier CBR sont plus prononcées à des vitesses de transmission inférieures. À des vitesses de transmission supérieures, la qualité d’un fichier encodé CBR continuera à varier, mais les problèmes de qualité seront moins perceptibles pour l’utilisateur. Lorsque vous utilisez l’encodage CBR, vous devez définir la bande passante aussi élevée que possible.

-   [Paramètres de Configuration CBR](#cbr-configuration-settings)
-   [Paramètres de compartiment avec fuites](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>Paramètres de Configuration CBR

Vous devez configurer un encodeur en spécifiant le type d’encodage et les différents paramètres spécifiques au flux avant la session d’encodage.

**Pour configurer l’encodeur pour l’encodage CBR**

1.  Spécifiez le mode d’encodage CBR.

    Par défaut, l’encodeur est configuré pour utiliser l’encodage CBR. La configuration de l’encodeur est définie via des valeurs de propriété. Ces propriétés sont définies dans wmcodecdsp. h. Vous pouvez spécifier explicitement ce mode en affectant à la propriété [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la \_ valeur variant false. Pour plus d’informations sur la façon de définir des propriétés sur des encodeurs, consultez [configuration de l'](configuring-the-encoder.md)encodeur.

2.  Choisissez la vitesse de transmission du codage.

    Pour l’encodage CBR, vous devez connaître la vitesse de transmission à laquelle vous souhaitez encoder le flux avant le début de la session de codage. Vous devez définir la vitesse de transmission pendant que vous configurez l’encodeur. Pour ce faire, pendant que vous effectuez la négociation de type de média, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) du type de données audio MF MT (pour les flux audio) ou la vitesse moyenne (pour les flux vidéo) des types de médias de sortie disponibles, puis choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission cible. [**\_ \_ \_**](mf-mt-avg-bitrate-attribute.md) Pour plus d’informations, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).

L’exemple de code suivant montre l’implémentation de SetEncodingProperties. Cette fonction définit les propriétés d’encodage de niveau flux pour CBR et VBR.


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a>Paramètres de compartiment avec fuites

Pour l’encodage CBR, la moyenne et les valeurs maximales de compartiment avec fuites pour le flux sont identiques. Pour plus d’informations sur ces paramètres, consultez [le modèle de tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md).

Pour encoder des flux audio CBR, vous devez définir les valeurs des compartiments de fuites après avoir négocié le type de média de sortie sur l’encodeur. L’encodeur calcule la fenêtre de mémoire tampon en interne en fonction de la vitesse de transmission moyenne définie sur le type de média de sortie.

Pour définir des valeurs de compartiment fuites, créez un tableau de DWORDs. vous pouvez définir les valeurs suivantes dans la propriété [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) dans la Banque de propriétés du récepteur multimédia. Pour plus d’informations, consultez [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).

-   Vitesse de transmission moyenne : obtient la vitesse de transmission moyenne à partir du type de média de sortie sélectionné lors de la négociation de type de média. Utilisez l' [**attribut \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de l’entrée de données audio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .
-   Fenêtre de mémoire tampon : interrogez l’encodeur pour l’interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) , puis appelez [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).
-   Taille de la mémoire tampon initiale : définie sur 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types d’encodage ASF](asf-encoding-types.md)
</dt> <dt>

[didacticiel : encodage de média de Windows Pass](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
