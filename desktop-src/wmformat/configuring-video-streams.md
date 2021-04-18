---
title: Configuration de flux vidéo
description: Configuration de flux vidéo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flux, configuration de flux vidéo
- codecs, configuration des flux vidéo
- flux vidéo, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512082"
---
# <a name="configuring-video-streams"></a>Configuration de flux vidéo

Les flux vidéo sont plus flexibles dans leur configuration que les flux audio. Cela est dû au fait que les propriétés des frames qui composent la vidéo peuvent varier considérablement d’un fichier à l’autre. Lorsque vous récupérez le format de codec du codec que vous utilisez, vous devez définir les valeurs suivantes pour les objets de configuration de flux vidéo.



| Valeur                                 | Description                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vitesse de transmission                              | Appelez [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) pour définir la valeur souhaitée. Le codec vidéo essaiera de compresser le média pour répondre à vos spécifications. Si vos valeurs sont trop basses, la vidéo compressée obtenue sera très détériorée.           |
| Fenêtre de mémoire tampon                         | Appelez [**IWMStreamConfig :: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) pour définir la valeur souhaitée. Le codec vidéo essaiera de compresser le média pour répondre à vos spécifications. Si vos valeurs sont trop basses, la vidéo compressée obtenue sera très détériorée. |
| **WMVIDEOINFOHEADER.rcSource**        | L’angle supérieur gauche doit avoir la valeur 0, 0. L’angle inférieur droit doit être défini sur les dimensions du cadre. Par exemple, dans un flux de 640 x 480, ces paramètres sont 0, 0640480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Doit correspondre à **rcSource**.                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Doit correspondre à la vitesse de transmission définie pour le flux.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Définissez sur le temps approximatif par cadre.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER. bichasse**          | Définissez sur la largeur, en pixels, de la taille de frame souhaitée.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER. bihauteur**         | Définissez sur la hauteur, en pixels, de la taille de trame souhaitée.                                                                                                                                                                                                                    |



 

Le contenu vidéo ne s’exécute pas correctement, sauf s’il est encodé à une taille qui est un multiple de quatre pour la largeur et la hauteur. L’exception est une vidéo [*RGB*](wmformat-glossary.md) non compressée, qui peut avoir n’importe quelle taille. Si vous essayez de définir une taille qui n’est pas un multiple de quatre, l’une des erreurs suivantes est retournée par le writer :

-   \_ \_ \_ format d’entrée NS E non valide \_
-   NS \_ E \_ \_ format de sortie non valide \_
-   \_INVALIDPROFILE NS E \_

Si vous utilisez un encodage à vitesse de transmission variable, vous devrez peut-être effectuer d’autres ajustements. Pour plus d’informations, consultez [Configuration des flux VBR](configuring-vbr-streams.md).

Certains codecs Windows Media Video prennent en charge plusieurs niveaux de complexité. Les niveaux de complexité déterminent les algorithmes qui seront utilisés par le codec lors de l’encodage d’un flux vidéo. L’utilisation d’un niveau de complexité élevé nécessitera davantage de puissance de traitement pour l’encodage et le décodage.

Chaque codec qui prend en charge les paramètres de complexité expose les paramètres suivants que vous pouvez récupérer à l’aide de la méthode [**IWMCodecInfo3 :: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .



| Paramètre                 | Description                                         |
|-------------------------|-----------------------------------------------------|
| \_wszComplexityMax g     | Niveau de qualité maximal pris en charge par le codec.   |
| \_wszComplexityOffline g | Niveau de qualité suggéré pour la lecture hors connexion.   |
| \_wszComplexityLive g    | Niveau de qualité suggéré pour la lecture en continu. |



 

Pour définir la complexité d’un flux vidéo dans un profil, utilisez la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) à l’aide de la propriété g \_ wszComplexity. La valeur que vous définissez doit être inférieure ou égale à la complexité maximale prise en charge pour le codec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> <dt>

[**Paramètres de complexité de la vidéo**](video-complexity-settings.md)
</dt> </dl>

 

 




