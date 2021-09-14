---
title: Codecs pris en charge
description: Codecs pris en charge
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK, codecs pris en charge
- Windows Media Format SDK, interface IWMCodecInfo3
- codecs, pris en charge
- IWMCodecInfo3, à propos de
- codecs, interface IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d202470e2fd430025c5c1e75d0677e4504189e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293814"
---
# <a name="supported-codecs"></a>Codecs pris en charge

le kit de développement logiciel (sdk) Windows Media Format prend en charge les codecs suivants, qui sont inclus lorsque vous installez le kit de développement logiciel (sdk).




| Codec | Description | 
|-------|-------------|
| Windows Media Audio | Codec audio pour une utilisation générale dans l’encodage de données audio complexes, telles que la musique. les versions les plus récentes de ce codec sont le codec Windows Media Audio 9 et le codec Windows Media Audio 9,1.<br /> | 
| Windows Professional multimédia audio | Codec audio pour des données audio complexes, telles que la musique. Prend en charge l’encodage multicanaux et 24 bits. Il existe deux versions de ce codec :<br /><ul><li>Windows Media Audio 9 Professional</li><li>Windows Média audio 9,1 Professional</li></ul> | 
| Windows Média audio sans perte | Codec audio pour l’encodage sans perte. Il existe deux versions de ce codec :<br /><ul><li>Windows Media Audio 9 sans perte</li><li>Windows Média audio 9,1 sans perte</li></ul> | 
| Windows Media Audio 9 voix | Codec audio optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit du codec préféré pour les flux composés principalement de mots prononcés. Pour le contenu mixte musical et vocal, ce codec peut modifier dynamiquement l’algorithme d’encodage utilisé pour obtenir une qualité optimale. | 
| Windows Media Video 9 | Codec vidéo pour une utilisation générale dans l’encodage d’une vidéo complexe, telle que des films. | 
| Windows Profil Media Video 9 Advanced | Codec vidéo incorporant des fonctionnalités d’encodage avancées, y compris l’encodage entrelacé. | 
| Windows Écran Media Video 9 | Codec vidéo optimisé pour l’encodage des captures d’écran séquentielles. Ce codec est souvent utilisé pour la formation ou le support logiciel en enregistrant des images de moniteur à mesure que des applications d’ordinateur sont utilisées. | 
| Windows Image de la vidéo multimédia | Codec vidéo pour convertir des images bitmap avec des informations de déformation en vidéo compressée. Il existe deux versions de ce codec :<br /><ul><li>Windows Image Media Video 9</li><li>Windows Media Video 9 image v2</li></ul> | 




 

différentes versions des codecs vidéo et Windows Media Audio sont disponibles pour l’encodage en fonction de la version du kit de développement logiciel (SDK) Windows Media Format que vous installez. Lorsque vous utilisez les méthodes si l’interface [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) pour énumérer les codecs et les formats de codec, seules les dernières versions prises en charge sont énumérées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Choix d’une méthode d’encodage**](choosing-an-encoding-method.md)
</dt> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> </dl>

 

 





