---
description: Décodage
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Décodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bfef7fe219ae7ff05227bfba48b69188844dc2373bd1c3099737224758fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667326"
---
# <a name="decoding"></a>Décodage

Pour prendre en charge correctement les métadonnées, les auteurs des décodeurs doivent effectuer les opérations suivantes :

-   Implémentez des interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .
-   Implémentez [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sur le décodeur de trame. Si le codec prend en charge les métadonnées au niveau du conteneur, cette interface doit être implémentée sur le décodeur au niveau du conteneur, ainsi que sur le décodeur de trame.
-   Lors du décodage du flux d’image, appelez [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) pour instancier un lecteur de métadonnées pour chaque bloc de métadonnées. (Tous les nouveaux lecteurs de métadonnées implémentés par le codec doivent être inscrits auprès de WIC.)

    Le décodeur ne doit pas créer ses propres lecteurs de métadonnées, mais plutôt utiliser le WIC pour les créer en fonction des blocs de métadonnées dans le flux. Le décodeur doit le faire sur tous les blocs qu’il trouve, même s’ils ne sont pas connus de façon native du code, car les lecteurs de métadonnées futurs peuvent être installés sur le système et comprendre comment gérer ces blocs de métadonnées.

-   S’il n’existe aucun gestionnaire de métadonnées pour un bloc, instanciez le lecteur de métadonnées inconnu à l’aide des options de création de métadonnées.
-   Exposez la collection de lecteurs de métadonnées via l’interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



