---
description: 'Dans la vitesse de transmission variable (VBR), le contenu est encodé à une vitesse de transmission et à des valeurs maximales spécifiées : une vitesse de transmission maximale et une fenêtre de mémoire tampon de pointe.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Encodage à vitesse de transmission variable Peak-Constrained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531117"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Encodage à vitesse de transmission variable Peak-Constrained

Dans la vitesse de transmission variable (VBR), le contenu est encodé à une vitesse de transmission et à des *valeurs maximales* spécifiées : une vitesse de transmission maximale et une fenêtre de mémoire tampon de pointe. Ces valeurs de pic sont également appelées les *valeurs de plage de pics de fuites*. Le fichier est encodé pour se conformer à une mémoire tampon décrite par les valeurs de pic, de sorte que la vitesse de transmission moyenne globale du flux est égale ou inférieure à la valeur de vitesse de transmission moyenne que vous avez spécifiée.

En règle générale, le taux binaire de pointe est assez élevé. L’encodeur garantit que la valeur de la vitesse de transmission moyenne spécifiée est conservée pendant la durée du flux (vitesse de transmission moyenne >= (taille totale du flux en bits/durée en secondes)). Prenons l’exemple suivant : vous configurez un flux avec une vitesse de transmission moyenne de 16 000 bits par seconde, un taux de bits de pic de 48 000 bits par seconde et une fenêtre de mémoire tampon de pointe de 3 000 (3 secondes). La taille de la mémoire tampon utilisée pour le flux est de 144 000 bits (48 000 bits par seconde \* 3 secondes), comme déterminé par les valeurs de pic. L’encodeur compresse les données pour se conformer à cette mémoire tampon. En outre, la vitesse de transmission moyenne du flux doit être inférieure ou égale à 16 000. Si l’encodeur doit créer des échantillons de grande taille pour gérer un segment de contenu complexe, il peut tirer parti de la grande taille de mémoire tampon. Toutefois, d’autres parties du flux doivent être encodées à une vitesse de transmission inférieure pour ramener la moyenne au niveau spécifié. L’encodage VBR maximal limité est utile pour les périphériques de lecture avec une capacité de mémoire tampon finie et des contraintes de débit de données. Un exemple courant est l’encodage utilisé pour les DVD quand le décodage est effectué par une puce dans un appareil, où des limitations matérielles doivent être prises en compte.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configuration de l’encodeur pour Peak-Constrained VBR

Le VBR limité au maximum est comme un VBR non [restreint](unconstrained-variable-bit-rate--vbr--encoding.md) en ce qu’il est limité à un débit binaire moyen sur la durée du flux. En outre, le VBR maximal restreint est conforme à une mémoire tampon de pointe. Cette mémoire tampon est décrite à l’aide d’une vitesse de pointe et d’une fenêtre de tampon de pointe. Ce mode utilise deux passes d’encodage et donne à l’encodeur la flexibilité nécessaire pour coder les exemples individuels tout en adhérant aux limitations de pointe.

La configuration de l’encodeur est définie via des valeurs de propriété. Ces propriétés sont définies dans wmcodecdsp. h. Les propriétés de configuration doivent être définies sur l’encodeur avant de négocier le type de média de sortie. Pour plus d’informations sur la façon de définir des propriétés sur l’encodeur, consultez [configuration de l’encodeur](configuring-the-encoder.md). En fonction des valeurs de propriété spécifiées, vous pouvez énumérer les types de sortie VBR pris en charge et sélectionner celui qui est requis sur l’encodeur [Media Foundation transformer](media-foundation-transforms.md) (MFT) en fonction de la vitesse de transmission moyenne.

Vous devez définir les Propertiesfor suivants pour ce type d’encodage :

-   Spécifiez le mode d’encodage VBR en affectant \_ à la propriété MFPKEY VBRENABLED la \_ valeur variant true.
-   Affectez la valeur \_ 2 à MFPKEY PASSESUSED, car le mode VBR avec un pic restreint utilise deux passes d’encodage.
-   Définissez MFPKEY \_ Rmax pour spécifier la vitesse de transmission maximale et définissez MFPKEY \_ BMAX pour spécifier la fenêtre de mémoire tampon de pointe.
-   Lors de l’énumération du type de média de sortie, vérifiez l’attribut [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) (pour les flux audio) et le débit moyen des signaux audio (pour les flux vidéo) de sortie, puis choisissez un type de média de sortie dont le débit moyen est le plus proche de la vitesse de transmission moyenne souhaitée que l’encodeur doit conserver dans le contenu encodé. [**\_ \_ \_**](mf-mt-avg-bitrate-attribute.md) Pour plus d’informations sur la sélection du type de média de sortie, consultez [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Il est recommandé de définir le taux de bits de pointe sur au moins deux fois la vitesse de transmission moyenne. Le fait de définir le taux de pic sur une valeur inférieure peut entraîner l’encodeur à encoder le contenu sous la forme d’un CBR à deux passes au lieu du VBR avec un pic restreint.

 

Pour récupérer la valeur de la fenêtre de mémoire tampon définie par l’encodeur, appelez **IWMCodecLeakyBucket :: GetBufferSizeBits**, défini dans wmcodecifaces. h, wmcodecdspuuid. lib, après la session d’encodage. Pour ajouter une prise en charge VBR sans contrainte pour les flux, vous devez définir cette valeur dans l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valeurs de compartiment avec fuite de pic) sur l’objet de configuration de flux lors de la configuration du profil ASF.

L’exemple de code suivant modifie la méthode SetEncodingType de l’exemple de classe CEncoder pour configurer le mode VBR avec des pics de charge. Pour plus d’informations sur cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md). Pour plus d’informations sur les macros d’assistance utilisées dans cet exemple, consultez Utilisation des exemples de code Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
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

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
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

[comment créer une topologie pour Two-Pass l’encodage de média Windows](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



