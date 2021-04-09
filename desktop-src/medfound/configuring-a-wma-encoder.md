---
description: Définition d’un type de sortie pour un encodeur WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Définition d’un type de sortie pour un encodeur WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111846"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Définition d’un type de sortie pour un encodeur WMA

Pour créer un type de sortie valide pour un encodeur Windows Media Audio (WMA), vous devez disposer des informations suivantes :

-   Sous-type audio qui repesents le format WMA encodé. Consultez [GUID de sous-type audio](audio-subtype-guids.md).
-   Propriétés de configuration à définir sur l’encodeur.

    Les propriétés de configuration sont documentées dans la documentation Windows Media Audio et le codec vidéo et les API DSP. Pour plus d’informations, consultez « Propriétés des flux audio » dans [Propriétés de codage](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista ou version ultérieure

Pour obtenir un type de sortie valide pour l’encodeur, procédez comme suit.

1.  Utilisez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour créer une instance de l’encodeur.
2.  Interrogez l’encodeur pour l’interface **IPropertyStore** .
3.  Utilisez l’interface **IPropertyStore** pour configurer l’encodeur.
4.  Récupérez les types de sortie pris en charge en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) dans une boucle jusqu’à ce que l’encodeur retourne **MF E plus de \_ \_ \_ \_ types** et que vous choisissiez le type de média cible. I
5.  Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.

### <a name="windows-7"></a>Windows 7

Pour obtenir un type de sortie valide pour l’encodeur dans Windows 7, Media Foundation fournit la fonction [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Une application doit passer le sous-type audio qui repesents le WMA encodé et les propriétés d’encodage. Les propriétés sont obligatoires, car l’encodeur modifie les types de sortie pris en charge en fonction du mode défini.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)est uniquement pris en charge pour un [encodage à vitesse binaire constante](constant-bit-rate-encoding.md).

 

Si l’appel s’effectue correctement, l’application reçoit une liste de pointeurs IUnknown des types de supports de sortie pris en charge dans un objet [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) . Pour définir le type de média de sortie, recherchez celui qui correspond à votre type cible et appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Encodeurs Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



