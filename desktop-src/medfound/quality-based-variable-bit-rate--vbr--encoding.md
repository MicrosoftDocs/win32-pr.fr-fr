---
description: Encodage à vitesse de transmission variable Quality-Based
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Encodage à vitesse de transmission variable Quality-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524944"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Encodage à vitesse de transmission variable Quality-Based

Contrairement à l' [encodage à débit binaire constant](constant-bit-rate-encoding.md) (CBR), où l’encodeur s’efforce de maintenir une vitesse de transmission particulière du média encodé, en mode VBR (variable bit rate), l’encodeur s’efforce d’obtenir la meilleure qualité possible du média encodé. La principale différence entre CBR et VBR est la taille de la fenêtre de mémoire tampon utilisée. Les flux encodés VBR ont généralement des fenêtres de tampon volumineuses par rapport aux flux encodés CBR.

La qualité du contenu encodé est déterminée par la quantité de données perdues lorsque le contenu est compressé. De nombreux facteurs affectent la perte de données dans le processus de compression ; mais en général, plus les données d’origine sont complexes et plus le taux de compression est élevé, plus le processus de compression est détaillé.

En mode VBR basé sur la qualité, vous ne définissez pas une vitesse de transmission ou une fenêtre de mémoire tampon que l’encodeur doit suivre. Au lieu de cela, vous spécifiez un niveau de qualité pour un flux multimédia numérique au lieu d’une vitesse de transmission. L’encodeur compresse le contenu afin que tous les échantillons soient de qualité comparable. Cela garantit la cohérence de la qualité tout au long de la durée de la lecture, indépendamment des exigences de mémoire tampon du flux résultant.

L’encodage VBR basé sur la qualité tend à créer de grands flux compressés. En général, ce type d’encodage est bien adapté à la lecture locale ou aux connexions réseau à bande passante élevée (ou téléchargement et lecture). Par exemple, vous pouvez écrire une application pour copier des chansons de fichiers CD vers ASF sur un ordinateur. L’utilisation de l’encodage VBR basé sur la qualité garantit que toutes les chansons copiées sont de la même qualité. Dans ce cas, la qualité cohérente offre une meilleure expérience utilisateur.

L’inconvénient du codage VBR basé sur la qualité est qu’il n’existe aucun moyen de connaître les exigences de taille ou de bande passante des médias encodés avant la session d’encodage, car l’encodeur utilise une seule passe d’encodage. Cela peut rendre les fichiers au format VBR basés sur la qualité inappropriés pour les cas où la mémoire ou la bande passante sont restreintes, par exemple pour la lecture de contenu sur des lecteurs multimédias portables ou la diffusion en continu sur un réseau à faible bande passante.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Configuration de l’encodeur pour l’encodage Quality-Based VBR

La configuration de l’encodeur est définie via des valeurs de propriété. Ces propriétés sont définies dans wmcodecdsp. h. Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie. Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md).

La liste suivante répertorie les propriétés que vous devez définir pour ce type d’encodage :

-   Spécifiez le mode d’encodage VBR en affectant à la propriété **MFPKEY \_ VBRENABLED** la \_ valeur variant true.
-   Affectez la valeur 1 à **MFPKEY \_ PASSESUSED** , car ce mode VBR utilise une seule passe d’encodage.
-   Définissez le niveau de qualité souhaité (de 0 à 100) en définissant la propriété **MFPKEY \_ souhaitée \_ VBRQUALITY** . La fonction VBR basée sur la qualité n’encode pas le contenu dans des paramètres de mémoire tampon prédéfinis. Ce niveau de qualité sera conservé pour l’ensemble du flux, indépendamment des exigences de vitesse de transmission qui en résultent.
-   Pour les flux vidéo, définissez la vitesse de transmission moyenne sur une valeur différente de zéro dans l’attribut de [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média de sortie de l’encodeur. La vitesse de transmission exacte est mise à jour une fois la session de codage terminée.

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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types d’encodage ASF](asf-encoding-types.md)
</dt> </dl>

 

 



