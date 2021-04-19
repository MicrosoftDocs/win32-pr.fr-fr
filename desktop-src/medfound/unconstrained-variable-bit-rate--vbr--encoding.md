---
description: Encodage de la vitesse de transmission variable sans contrainte
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Encodage de la vitesse de transmission variable sans contrainte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524986"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a>Encodage de la vitesse de transmission variable sans contrainte

Dans le mode d’encodage VBR (variable bit rate) sans contrainte, le contenu est encodé à la qualité la plus élevée possible tout en conservant une vitesse de transmission spécifiée.

L’encodage VBR sans contrainte utilise deux passes d’encodage. Lorsque vous utilisez l’encodage VBR non restreint, vous spécifiez une vitesse de transmission pour le flux, comme vous le feriez avec un [encodage à débit binaire constant](constant-bit-rate-encoding.md). Toutefois, l’encodeur utilise cette valeur uniquement comme la vitesse de transmission moyenne pour le flux et l’encodage afin que la qualité soit aussi élevée que possible tout en conservant la moyenne. Les échantillons individuels produits par l’encodeur varient en fonction de la taille sans limite de mémoire tampon explicite. Toutefois, la vitesse de transmission moyenne pendant la session d’encodage et la durée du flux ne doivent pas être supérieures à la valeur que vous avez spécifiée. La vitesse de transmission réelle à n’importe quel point dans le flux encodé peut varier considérablement de la valeur moyenne. Vous ne définissez pas de fenêtre de mémoire tampon pour l’encodage VBR sans contrainte. Au lieu de cela, l’encodeur calcule la taille de la fenêtre de mémoire tampon requise en fonction des spécifications des exemples encodés. Cela signifie qu’il n’existe aucune limite à la taille des échantillons individuels dans le flux, tant que la vitesse de transmission moyenne est inférieure ou égale à la valeur que vous avez définie.

L’avantage d’un encodage VBR non restreint est que le flux compressé a la qualité la plus élevée possible tout en restant dans une bande passante moyenne prévisible. Utilisez cette valeur lorsque vous devez spécifier une bande passante, mais que des fluctuations autour de la bande passante spécifiée sont acceptables. par exemple, pour les fichiers locaux ou uniquement pour le téléchargement.

L’inconvénient de ce mode de codage est que l’encodeur peut définir la fenêtre de mémoire tampon sur la valeur requise après l’encodage, ce qui vous permet de contrôler la taille de la mémoire tampon. Dans la plupart des cas, si vous ne vous inquiétez pas de la taille de la mémoire tampon ou de la cohérence de l’utilisation de la bande passante, vous devez utiliser l' [encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md) .

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Configuration de l’encodeur pour le VBR non restreint

La configuration de l’encodeur est définie via des valeurs de propriété. Ces propriétés sont définies dans wmcodecdsp. h. Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie. Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md). En fonction des valeurs de propriété spécifiées, vous pouvez énumérer les types de sortie VBR pris en charge et sélectionner celui qui est requis sur l’encodeur [Media Foundation transformer](media-foundation-transforms.md) (MFT) en fonction de la vitesse de transmission moyenne.

La liste suivante répertorie les propriétés que vous devez définir pour ce type d’encodage :

-   Spécifiez le mode d’encodage VBR en affectant \_ à la propriété MFPKEY VBRENABLED la \_ valeur variant true.
-   Affectez la valeur \_ 2 à MFPKEY PASSESUSED, car le mode VBR sans contrainte utilise deux passes d’encodage.
-   Lors de l’énumération du type de média de sortie, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde des octets audio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (pour les flux audio) ou l’attribut vitesse de [**\_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) (pour les flux vidéo) des types de supports de sortie disponibles. Choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission moyenne souhaitée que vous souhaitez que l’encodeur conserve dans le contenu encodé. Pour plus d’informations sur la sélection du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).

Pour faire en sorte que la valeur de la fenêtre de mémoire tampon soit définie par l’encodeur, appelez **IWMCodecLeakyBucket :: GetBufferSizeBits**, défini dans wmcodecifaces. h et wmcodecdspuuid. lib, après la session d’encodage. Pour ajouter une prise en charge VBR sans contrainte pour les flux, vous devez définir cette valeur dans l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valeurs de compartiment de fuite moyenne) sur l’objet de configuration de flux lors de la configuration du profil ASF.

La commande suivante modifie la méthode SetEncodingType de l’exemple de classe CEncoder pour configurer le mode VBR sans contrainte. Pour plus d’informations sur cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md). Pour plus d’informations sur les macros d’assistance utilisées dans cet exemple, consultez Utilisation des exemples de code Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types d’encodage ASF](asf-encoding-types.md)
</dt> <dt>

[Modèle de mémoire tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Comment créer une topologie pour Two-Pass l’encodage Windows Media](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



