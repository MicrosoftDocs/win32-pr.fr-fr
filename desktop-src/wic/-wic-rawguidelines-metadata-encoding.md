---
description: Encodage
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: encodage (composant de création d’images Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964648"
---
# <a name="encoding-windows-imaging-component"></a>encodage (composant de création d’images Windows)

L’auteur de l’encodeur doit effectuer les opérations suivantes :

-   Implémentez des interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .
-   Implémentez [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur l’encodeur de trame. Si le codec prend en charge les métadonnées au niveau du conteneur, cette interface doit être implémentée sur l’encodeur au niveau du conteneur, ainsi que sur l’encodeur de trame.
-   Si le format de conteneur contient implicitement des blocs de métadonnées obligatoires, instanciez un générateur de métadonnées pour chaque bloc de ce type. Par exemple, le format TIFF requiert un appareil d’interface (IFD) pour chaque trame, de sorte que l’enregistreur IFD doit toujours être exposé.
-   Implémentez la prise en charge de la gestion de la collection des enregistreurs de métadonnées. Le writer de bloc gère les exigences de commande ou les restrictions de conteneur sur les types de blocs de métadonnées qui peuvent être encodés. Le writer de bloc doit vérifier que tous les nouveaux enregistreurs de métadonnées peuvent être incorporés dans le format de conteneur.
-   Lors de l’encodage du flux d’image, appelez [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) pour sérialiser le contenu de chaque générateur de métadonnées dans le flux. Si le bloc de métadonnées contient des métadonnées « critiques », l’encodeur doit définir les éléments de métadonnées critiques avant de demander au writer de métadonnées de sérialiser le contenu.
-   Vérifiez la présence de gestionnaires de métadonnées inconnus pour vous assurer que les blocs de métadonnées redondants ne sont pas présents. Cela est important car, tout en préservant les métadonnées dans un scénario de décodage ou de codage, les blocs inconnus peuvent être un doublon de blocs de métadonnées obligatoires.

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

 

 



