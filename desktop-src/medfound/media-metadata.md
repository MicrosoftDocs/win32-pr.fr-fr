---
description: Métadonnées de média
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Métadonnées de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef9f8a852bbce2dfb8d38a5883acc219cde8019
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477084"
---
# <a name="media-metadata"></a>Métadonnées de média

Les fichiers multimédias contiennent des propriétés qui décrivent le contenu du fichier. Dans Microsoft Media Foundation, ces propriétés peuvent être classées comme suit :

-   Les **attributs de type de média** spécifient les paramètres d’encodage, tels que l’algorithme d’encodage (sous-type de média), la taille d’image vidéo, la fréquence d’images vidéo, la vitesse de transmission audio et le taux d’échantillonnage audio. Pour plus d’informations sur les attributs de type de média, consultez [types de médias](media-types.md).
-   Les **métadonnées** contiennent des informations descriptives sur le contenu multimédia, telles que le titre, l’artiste, le compositeur et le genre. Les métadonnées peuvent également décrire les paramètres d’encodage. Il peut être plus rapide d’accéder à ces informations par le biais de métadonnées que par le biais d’attributs de type média.
-   Les **Propriétés DRM** contiennent des informations sur les restrictions d’utilisation. Actuellement Media Foundation ne prend pas en charge les propriétés DRM par le biais de métadonnées, à l’exception de la propriété **\_ hyperdrm \_ IsProtected** .

Il existe deux façons de lire les métadonnées dans Media Foundation :

-   Interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (métadonnées de la version 1 Media Foundation).
-   interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de l’interpréteur de commandes Windows (métadonnées de shell).

Les métadonnées de l’interpréteur de commandes se rapportent non seulement aux fichiers multimédias, mais à un plus grand nombre de fichiers sur le système.

Le tableau suivant compare les fonctionnalités et les limitations de chaque API de métadonnées.




| Media Foundation les métadonnées v1 | Métadonnées de Shell | 
|------------------------------|----------------|
| requiert Windows Vista ou version ultérieure. | requiert Windows 7.<blockquote>[!Note]<br />en général, les métadonnées de l’interpréteur de commandes ne nécessitent pas de Windows 7, mais Media Foundation ne prenait pas en charge les métadonnées d’environnement antérieures à Windows 7.</blockquote><br /> | 
| Les propriétés ne sont pas compatibles avec le système de propriétés de Shell. | Les propriétés sont compatibles avec le système de propriétés de Shell. | 
| Les propriétés peuvent s’appliquer à la totalité du fichier ou au niveau du flux. | Seules les propriétés au niveau du fichier sont prises en charge. Les propriétés au niveau du flux ne sont pas prises en charge. | 
| Les propriétés peuvent avoir des valeurs dans plusieurs langues. | Les valeurs dans plusieurs langues ne sont pas prises en charge. | 
| Les clés de propriété sont des chaînes à caractères larges. | Les clés de propriété sont des valeurs <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> . | 
| Les valeurs de propriété sont des valeurs <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> . | Les valeurs de propriété sont des valeurs <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> . | 




 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Fournisseurs de métadonnées de Shell](shell-metadata-providers.md)<br/>                       | à partir de Windows 7, Media Foundation expose des métadonnées par le biais de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .<br/> |
| [Propriétés de métadonnées pour les fichiers multimédias](metadata-properties-for-media-files.md)<br/> | Cette rubrique répertorie les propriétés de métadonnées les plus courantes pour les fichiers multimédias.<br/>                                                           |
| [fournisseurs de métadonnées dans Windows Vista](metadata-providers-in-windows-vista.md)<br/> | dans Windows Vista, Media Foundation expose des métadonnées par le biais de l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .<br/>                   |



 

Si vous implémentez une source de média personnalisée et souhaitez exposer les métadonnées de l’interpréteur de commandes, consultez [fournisseurs de métadonnées personnalisés pour les fichiers multimédias](custom-metadata-providers-for-media-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
