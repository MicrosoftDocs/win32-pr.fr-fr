---
title: Pour énumérer les formats de codec
description: Pour énumérer les formats de codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flux, énumération des formats de codec
- codecs, énumérations
- flux, formats de codec
- codecs, formats
- codecs, interface IWMCodecInfo
- IWMCodecInfo, formats de codec
- codecs, interface IWMCodecInfo3
- IWMCodecInfo3, formats de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221b675c5aa3b5602bcfda96b22233f77d4ba92199f29f36885a4053700dfd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196515"
---
# <a name="to-enumerate-codec-formats"></a>Pour énumérer les formats de codec

Un format de codec est un objet de configuration de flux rempli avec les données d’un codec. Chaque format de codec contient une configuration de média prise en charge par le codec. La plupart des codecs audio prennent en charge un nombre fini de formats, chacun d’entre eux étant énuméré par le codec et accessible à l’aide des méthodes de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). En revanche, les codecs vidéo ne fournissent qu’un seul format. Cela est dû au fait que les flux vidéo ont des variables, comme la taille du cadre, qui sont plus flexibles que les paramètres d’un flux audio. Avec un flux vidéo, vous devez remplir certaines des valeurs de configuration de flux. les configurations de flux audio ne doivent être modifiées que pour assigner un nom, un nom de connexion et un numéro de flux. Pour plus d’informations, consultez [configuration commune à tous les flux](configuration-common-to-all-streams.md).

Les formats de codec énumérés dépendent des paramètres d’énumération de codec actuels, qui sont définis à l’aide de [**IWMCodecInfo3 :: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Seules deux propriétés de codec sont actuellement prises en charge : g \_ wszNumPasses, qui spécifie le nombre de passes d’encodage effectuées par le codec et g \_ wszVBREnabled, qui spécifie si le codec utilise l’encodage à vitesse de transmission variable. Le nombre maximal de passes d’encodage pris en charge par l’un des codecs est de deux. il existe donc quatre configurations distinctes pour lesquelles vous pouvez récupérer des codecs, comme indiqué dans le tableau suivant.



|    &nbsp;    | Flux CBR (constant bit rate) | 2-passer le flux CBR | Débit binaire variable (VBR) basé sur la qualité | Flux VBR basé sur la fréquence de bits (contraint ou non contraint) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| \_wszVBREnabled g | FALSE                          | false             | VRAI                                         | TRUE                                                     |
| \_wszNumPasses g  | 1                              | 2                 | 1                                            | 2                                                        |



 

Pour énumérer les formats pris en charge pour un codec, utilisez [**IWMCodecInfo :: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) pour rechercher le nombre de codecs pris en charge. Appelez ensuite [**IWMCodecInfo :: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) pour chaque format. Les index de format sont compris entre zéro et un nombre inférieur au nombre total de formats pris en charge. Vous pouvez récupérer une description du format en appelant [**IWMCodecInfo2 :: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Lorsque vous utilisez **GetCodecFormatDesc**, vous n’avez pas besoin d’utiliser **GetCodecFormat**, car l’objet de configuration de flux est récupéré par les deux méthodes. Les formats de codec vidéo n’incluent pas de description. Chaque codec vidéo n’a qu’un seul format utilisé pour tous les flux de ce type.

Lorsque vous récupérez un format de codec, vous accédez à l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) d’un objet de configuration de flux contenant les paramètres de mise en forme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Obtention d’informations de configuration de flux à partir de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




