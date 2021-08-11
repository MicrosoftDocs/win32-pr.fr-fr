---
description: Attributs du lecteur source
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Attributs du lecteur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238327"
---
# <a name="source-reader-attributes"></a>Attributs du lecteur source

Les attributs suivants peuvent être utilisés pour initialiser le [lecteur source](source-reader.md).



| Attribut                                                                                                            | Description                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_latence faible \_ MF](mf-low-latency.md)                                                                               | Active le traitement à faible latence.                                                                                                                                                                                                    |
| [\_ \_ convertisseurs de désactivation MF ReadWrite \_](mf-readwrite-disable-converters.md)                                            | Active ou désactive les conversions de format par le lecteur source.                                                                                                                                                                       |
| [MF \_ ReadWrite \_ activer \_ les \_ transformations matérielles](mf-readwrite-enable-hardware-transforms.md)                           | Permet au lecteur source d’utiliser des transformations de Media Foundation basées sur le matériel (MFTs).                                                                                                                                                |
| [\_ \_ rappel asynchrone du lecteur source \_ MF \_](mf-source-reader-async-callback.md)                                           | Contient un pointeur vers l’interface de rappel de l’application pour le lecteur source.                                                                                                                                                  |
| [\_ \_ Gestionnaire D3D du lecteur source \_ MF \_](mf-source-reader-d3d-manager.md)                                                 | Contient un pointeur vers le [Gestionnaire de périphériques Microsoft Direct3D](direct3d-device-manager.md).                                                                                                                                        |
| [\_lecteur source MF- \_ \_ désactiver \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Spécifie si le lecteur source active DirectX Video Acceleration (DXVA) sur le décodeur vidéo.                                                                                                                                |
| [\_ \_ le lecteur source MF \_ déconnecte \_ MEDIASOURCE à l' \_ \_ arrêt](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Spécifie si le lecteur source arrête la source du média.<br/> S’applique uniquement lorsque l’application crée le lecteur source à partir d’un objet source multimédia existant.<br/>                                           |
| [\_lecteur source \_ MF \_ activer \_ le \_ traitement vidéo avancé \_](mf-source-reader-enable-advanced-video-processing.md)     | Active le traitement vidéo avancé par le [lecteur source](source-reader.md), notamment la conversion de l’espace colorimétrique, le désentrelacement, le redimensionnement vidéo et la conversion de la fréquence d’images.                                                           |
| [le \_ lecteur source MF \_ \_ active le \_ \_ traitement vidéo](mf-source-reader-enable-video-processing.md)                        | Active le traitement vidéo limité par le lecteur source.                                                                                                                                                                             |
| [\_configuration du \_ lecteur de source \_ MF MF \_](mf-source-reader-mediasource-config.md)                                   | Contient les propriétés de configuration de la source du média.                                                                                                                                                                            |
| [\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_](mft-fieldofuse-unlock-attribute.md)                                            | Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , utilisé pour déverrouiller une table MFT avec des restrictions de champ d’utilisation. Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md). |



 

Utilisez ces attributs avec les méthodes et fonctions suivantes :

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Pour utiliser l’un de ces attributs, appelez d’abord [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs. Utilisez ensuite l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour définir les attributs souhaités sur le magasin d’attributs. Transmettez le pointeur **IMFAttributes** au paramètre *pAttributes* de l’une des méthodes ou fonctions indiquées précédemment.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




