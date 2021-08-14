---
title: Configuration de Flux
description: Configuration de Flux
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows Media Format SDK, Streams
- profils, flux
- flux, configuration
- codecs, configuration des flux
- profils, interface IWMStreamConfig
- flux, interface IWMStreamConfig
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199315"
---
# <a name="configuring-streams"></a>Configuration de Flux

La seule chose requise dans un profil est d’au moins un flux. Les autres options permettent d’accéder à des fonctionnalités plus avancées, mais avec au minimum un flux, vous pouvez créer un fichier ASF. Il est essentiel que vous compreniez comment configurer des flux avant de créer des profils complexes.

dans le cadre des profils, les flux peuvent être divisés en deux types : ceux qui sont compressés avec Windows codecs multimédias et des flux arbitraires qui ne sont pas traités avec des codecs. les flux Audio et vidéo sont les types qui utilisent les codecs de média Windows. Bien entendu, les flux peuvent contenir des fichiers audio ou vidéo compressés avec un codec tiers, mais le processus de configuration d’un tel flux est un cas particulier. Pour plus d’informations, consultez [pour créer des fichiers ASF à l’aide de codecs tiers](to-create-asf-files-using-third-party-codecs.md).

La liste suivante résume le processus de configuration d’un flux.

1.  Obtenez un objet de configuration de flux pour le flux.
    -   si vous créez un flux à l’aide de l’un des codecs de média Windows, vous devez obtenir l’objet de configuration de flux en tant que format de codec à l’aide des méthodes de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3).
    -   Si le flux est un type arbitraire, récupérez un objet de configuration de flux vide à l’aide de [**IWMProfile :: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configurez le flux pour répondre à vos besoins.
    -   un nom, un nom de connexion et un numéro de flux doivent être attribués à Flux de tous les types.
    -   les Flux à l’aide de Windows codecs multimédias ne doivent être modifiés que dans des formats prédéfinis à partir du format du codec. Pour les flux audio, seuls les paramètres de vitesse de transmission variable (VBR) pour le VBR en deux passes doivent être modifiés. Les flux vidéo doivent être configurés avec les propriétés de frame souhaitées.
    -   Les flux arbitraires ont des exigences de configuration variables par type. Tous requièrent une vitesse de transmission et une fenêtre de mémoire tampon.
3.  Ajoutez le flux au profil en appelant [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Tous les flux sont définis à l’aide d’objets de configuration de flux. L’interface principale d’un objet de configuration de flux est [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), qui fournit des méthodes pour définir les paramètres de base d’un flux, tels que le numéro de flux, la vitesse de transmission, etc. **IWMStreamConfig** est héritée par les interfaces plus récentes, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) et [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Comme pour toutes les révisions d’interface numérotées, vous devez toujours récupérer la version la plus récente à l’aide de la méthode **QueryInterface** .

La plupart des paramètres d’un flux sont accessibles par le biais de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). Ces paramètres sont encapsulés dans une structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Pour l’audio et la vidéo, la structure du **\_ \_ type de média WM** pointe vers une autre structure avec des informations supplémentaires spécifiques au type de média. Cette structure secondaire est généralement [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) pour l’audio et la [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) pour la vidéo. En outre, les flux vidéo ont une structure tertiaire, **BITMAPINFOHEADER**, qui décrit les caractéristiques d’un cadre de vidéo individuel. **BITMAPINFOHEADER** est une structure commune et se trouve dans la section Graphics Device Interface (GDI) du kit de développement logiciel (SDK) de plateforme.

Les sections suivantes décrivent comment configurer des flux.



| Section                                                                                                          | Description                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuration commune à tous les Flux](configuration-common-to-all-streams.md)                                   | Décrit la configuration de flux de base commune à tous les types de flux.                                                                                        |
| [Obtention d’informations de configuration de flux à partir de codecs](getting-stream-configuration-information-from-codecs.md) | décrit comment obtenir des informations de configuration de flux à partir des codecs pour garantir une configuration correcte des flux à l’aide des codecs Windows Media Audio et vidéo. |
| [Configuration de l’Flux audio](configuring-audio-streams.md)                                                       | Décrit comment configurer des flux audio.                                                                                                                       |
| [Configuration de la vidéo Flux](configuring-video-streams.md)                                                       | Décrit comment configurer les flux vidéo.                                                                                                                       |
| [configuration de Flux vidéo pour la recherche de performances](configuring-video-streams-for-seeking-performance.md)       | Décrit comment configurer des flux vidéo pour lesquels une recherche efficace est importante.                                                                              |
| [Configuration de la capture d’écran Flux](configuring-screen-capture-streams.md)                                     | Décrit comment configurer des flux vidéo pour la capture d’écran.                                                                                                    |
| [Configuration de l’image Flux](configuring-image-streams.md)                                                       | Décrit comment configurer des flux d’images.                                                                                                                       |
| [Utilisation de l’audio et de la vidéo non compressés Flux](using-uncompressed-audio-and-video-streams.md)                     | Décrit comment configurer un flux audio ou vidéo non compressé.                                                                                                  |
| [Configuration de types de flux arbitraires](configuring-arbitrary-stream-types.md)                                     | Décrit comment configurer des flux pour utiliser les types de flux arbitraires prédéfinis.                                                                                |
| [Configuration de VBR Flux](configuring-vbr-streams.md)                                                           | Décrit comment configurer des flux pour utiliser le codage à vitesse de transmission variable (VBR).                                                                                     |
| [Configuration d’extensions d’unité de données](configuring-data-unit-extensions.md)                                         | Décrit comment configurer un flux afin que les extensions d’unité de données puissent être jointes lors de l’écriture du fichier.                                                      |
| [Réutilisation des configurations de flux](reusing-stream-configurations.md)                                               | Décrit la façon dont vous pouvez utiliser des objets de configuration de flux à partir de profils existants pour créer de nouveaux profils.                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 