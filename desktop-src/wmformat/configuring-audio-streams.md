---
title: Configuration de l’Flux audio
description: Configuration de l’Flux audio
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- flux, configuration des flux audio
- codecs, configuration des flux audio
- flux audio, configuration
- codecs, formats
- flux, interface IWMCodecInfo
- IWMCodecInfo, flux audio
- flux, synchronisation A/V
- flux audio, synchronisation A/V
- Synchronisation A/V
- flux, synchronisation A/V
- flux audio, synchronisation A/V
- flux, formats audio à faible retards
- flux audio, formats audio à faible retards
- codecs, formats audio à faible retards
- flux, débit binaire variable (VBR)
- flux audio, débit binaire variable (VBR)
- codecs, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), configuration
- VBR (vitesse de transmission variable), configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522109"
---
# <a name="configuring-audio-streams"></a>Configuration de l’Flux audio

Les flux audio sont généralement les plus simples à configurer. Obtenez une configuration de flux à partir du codec à l’aide des méthodes de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) , comme décrit dans [obtention d’informations de configuration de flux à partir de codecs](getting-stream-configuration-information-from-codecs.md). Dans la plupart des cas, vous ne devez pas modifier les paramètres de ceux qui sont récupérés.

Le format de codec que vous sélectionnez parmi ceux qui sont énumérés dépend de l’utilisation prévue des fichiers ASF créés avec le profil. La description du format de codec récupérée par [**IWMCodecInfo2 :: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) résume les caractéristiques du format. Si votre application n’affiche pas les descriptions permettant de choisir entre elles, vous pouvez appeler **QueryInterface** sur l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) du format du codec pour obtenir l’interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) . Vous pouvez ensuite récupérer la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) en appelant [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). En examinant la structure du **\_ \_ type de média WM** et la structure [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) vers laquelle il pointe, vous pouvez déterminer les paramètres du format du codec et les comparer à vos besoins.

## <a name="getting-audio-formats-for-av-synchronization"></a>Obtention de formats audio pour la synchronisation A/V

le codec Windows Media Audio et Windows Media Audio Professional codec prennent en charge les formats pour les fichiers audio uniquement et pour les fichiers audio/vidéo. Les formats audio uniquement sont optimisés pour les fichiers contenant uniquement des données audio, tandis que les formats audio/vidéo sont optimisés pour l’audio qui se trouve dans un fichier avec un flux vidéo. Lors de l’énumération des formats de codec pour ces codecs, les formats audio/vidéo sont fournis après les formats audio uniquement. Les descriptions de format audio/vidéo contiennent toutes la chaîne « (A/V) ». Vous pouvez identifier les formats conçus pour la synchronisation audio/vidéo par programme en vérifiant le nombre de paquets par seconde. Les formats pour la synchronisation ont au moins 5 paquets par seconde si la vitesse de transmission est supérieure ou égale à 32 000 bits par seconde. Les formats avec des vitesses de bits inférieures à 32 000 bits par seconde peuvent être utilisés avec une vidéo synchronisée s’ils utilisent au moins 3 paquets par seconde. L’exemple de code de la rubrique [pour trouver les formats audio](to-find-audio-formats.md) contient le code requis pour effectuer cette vérification :


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Obtention de formats audio Low-Delay

le codec Windows Media 9,1 et le codec Windows Media Audio 9,1 Professional prennent en charge les formats à faible retard. Ces formats ont une fenêtre de mémoire tampon inférieure à celle des autres formats audio. L’audio à faible délai est conçu pour améliorer les performances dans les scénarios où les fichiers ou les flux sont souvent basculés. par exemple, une application qui répertorie un certain nombre de chansons pour la diffusion en continu dans l’interface utilisateur et permet aux utilisateurs de basculer de manière arbitraire entre eux.

Les formats à faible délai sont disponibles uniquement en mode CBR (un ou deux passes). Les descriptions de format à faible délai contiennent toutes la chaîne « délai faible ». Vous pouvez identifier les formats par programme en vérifiant la valeur de la vitesse de transmission du format. Les formats à faible délai sont affectés à des vitesses de transmission inférieures à 1 kilobits par rapport aux vitesses de transmission du format normal équivalent. par exemple, le codec Windows Media Audio 9,1 prend en charge un format CBR à passage unique avec une vitesse de transmission de 192 kbit/s. Le format à faible délai équivalent a une vitesse de transmission de 191 Kbits/s. en outre, à l’exception du format mono de 5 kbits/s pris en charge par le codec Windows Media Audio 9,1, les formats à faible délai sont les seuls formats qui ont une valeur de taux binaire impair.

## <a name="configuring-variable-bit-rate-audio"></a>Configuration de l’audio à vitesse de transmission variable

lorsque vous avez besoin d’un format VBR (variable bit rate) pour l’un des codecs audio Windows Media, vous pouvez l’obtenir en définissant les paramètres d’énumération dans la méthode [**IWMCodecInfo3 :: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) . Affectez la valeur \_ true à g wszVBREnabled et affectez la valeur 1 à g \_ wszNumPasses pour le VBR basé sur la qualité ou 2 pour le VBR en deux passes (contraint ou sans contrainte). Si vous utilisez le VBR à deux passes avec restriction, vous devez définir manuellement la vitesse de transmission maximale et la fenêtre de mémoire tampon pour le flux à l’aide des méthodes de [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) , comme décrit dans [configuration de VBR flux](configuring-vbr-streams.md).

Dans les profils VBR basés sur la qualité, le membre **nAvgBytesPerSec** de la structure **WAVEFORMATEX** contient le niveau de qualité (1 à 100) dans l’octet de poids faible et les trois octets de poids fort sont définis sur 0x7fffff. N’essayez pas de modifier le paramètre de qualité en modifiant cette valeur manuellement. vous devez utiliser le format tel qu’il est récupéré à partir du codec. Pour utiliser une valeur de qualité différente, vous devez énumérer les formats jusqu’à ce que vous en trouviez un qui réponde à vos besoins. En outre, **nAvgBytesPerSec** ne sera pas conservé dans le fichier ASF. Lorsque vous obtenez la structure **WAVEFORMATEX** pour un fichier qui a été ouvert avec l’objet Reader, **nAvgBytesPerSec** contient une valeur approximative représentant le nombre moyen d’octets par seconde.

> [!Note]  
> Quand vous configurez des flux audio, vous ne devez jamais avoir une valeur de fenêtre de mémoire tampon audio supérieure à la valeur de tous les flux vidéo dans le fichier. Normalement, ce n’est pas un problème, car les valeurs des fenêtres de mémoire tampon audio doivent être comprises entre 1,5 et 3 secondes, et les valeurs vidéo doivent être comprises entre 3 et 5 secondes. Si une fenêtre de mémoire tampon audio est supérieure à une fenêtre de mémoire tampon vidéo, le fichier est lu légèrement avec les flux, ce qui n’est pas le cas de la synchronisation.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> <dt>

[**Pour rechercher des formats audio**](to-find-audio-formats.md)
</dt> </dl>

 

 