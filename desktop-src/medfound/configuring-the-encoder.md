---
description: Propriétés d’encodage
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Propriétés d’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743491"
---
# <a name="encoding-properties"></a>Propriétés d’encodage

les encodeurs Windows Media Audio et Windows Media Video prennent en charge un large éventail de modes d’encodage. Ces modes sont généralement configurés en définissant des propriétés sur l’encodeur [Media Foundation transformer](media-foundation-transforms.md) (MFT). Pour effectuer un encodage de fichier, qu’il s’agisse d’utiliser des composants de niveau WMContainer ou de créer une topologie partielle, vous devez configurer l’encodeur de manière appropriée en définissant des propriétés en fonction du mode d’encodage et du type de média du flux. Le même ensemble de propriétés doit être défini à la fois sur l’encodeur et sur l’objet (récepteur de fichiers ASF ou multiplexeur ASF) que vous utilisez pour écrire le fichier ASF.

Les propriétés de l’encodeur sont définies dans wmcodecdsp. h. Les propriétés spécifiques utilisées pour configurer l’encodeur sont définies à l’aide des méthodes de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

-   [Propriétés du flux audio](#audio-stream-properties)
-   [Propriétés du flux vidéo](#video-stream-properties)
-   [Configuration de la Banque de propriétés de l’encodeur](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Propriétés du flux audio

Le tableau suivant présente les configurations d’encodeur pour un flux audio.



| Type d’encodage                                                                                        | Nom de la propriété-valeur                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Encodage à vitesse binaire constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (facultatif) par défaut, MFPKEY \_ VBRENABLED est défini sur **false**.<br/>                                                                                             |
| [Encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (facultatif)<br/> Par défaut, MFPKEY \_ PASSESUSED a la valeur 1.<br/> MFPKEY \_ souhaité \_ VBRQUALITY-de 0 à 100<br/> |
| [Encodage de la vitesse de transmission variable sans contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Chiffrement à vitesse de transmission variable à forte limite](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ Rmax-vitesse de transmission maximale<br/> MFPKEY \_ BMAX-fenêtre de mémoire tampon maximale<br/>                               |



 

### <a name="video-stream-properties"></a>Propriétés du flux vidéo

Le tableau suivant présente les configurations d’encodeur pour un flux vidéo.



| Type d’encodage                                                                                        | Nom de la propriété                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Encodage à vitesse binaire constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (facultatif)<br/> Par défaut, MFPKEY \_ VBRENABLED est défini sur **false**.<br/> MFPKEY \_ VIDEOWINDOW-fenêtre de mémoire tampon<br/>                                  |
| [Encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (facultatif)<br/> Par défaut, MFPKEY \_ PASSESUSED a la valeur 1.<br/> MFPKEY \_ souhaité \_ VBRQUALITY-de 0 à 100<br/> |
| [Encodage de la vitesse de transmission variable sans contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Chiffrement à vitesse de transmission variable à forte limite](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ Rmax-vitesse de transmission maximale<br/> MFPKEY \_ BMAX-fenêtre de mémoire tampon maximale<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configuration de la Banque de propriétés de l’encodeur

Vous devez configurer un encodeur en spécifiant le type d’encodage et les différents paramètres spécifiques au flux avant la session d’encodage. Vous devez également définir les propriétés de l’encodeur dans la Banque de propriétés d’un [objet ASF ContentInfo](asf-contentinfo-object.md) qui représente l’objet d’en-tête ASF du fichier de sortie.

Si vous utilisez une table MFT d’encodeur :

1.  Obtenir une référence à l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de la MFT de l’encodeur, comme décrit dans utilisation de l' [interface IMFTransform d’un encodeur](using-an-encoder-s-imftransform--interface.md).
2.  Interrogation de la MFT d’encodeur pour l’interface **IPropertyStore** .
3.  Définition des propriétés requises en appelant **IPropertyStore :: SetValue**.

Si vous utilisez les objets d’activation d’encodeur intégrés et que vous avez déjà créé un récepteur de fichiers ASF configuré, vous pouvez passer la Banque de propriétés du récepteur de média ASF à [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). L’encodeur est configuré automatiquement en fonction des paramètres spécifiés par l’application. Pour plus d’informations, consultez la procédure décrite dans [utilisation des objets d’activation d’un encodeur](using-an-encoder-s-activation-objects.md).

Pour plus d’informations sur la création d’objets Media Foundation à l’aide d’objets d’activation, consultez [objets d’activation](activation-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> </dl>

 

 
