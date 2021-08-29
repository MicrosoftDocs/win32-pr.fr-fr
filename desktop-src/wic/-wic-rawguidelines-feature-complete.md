---
description: 'Exhaustivité des fonctionnalités : interfaces recommandées'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Exhaustivité des fonctionnalités : interfaces recommandées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e3a01ae7a4ba0502ad76d03602a176ed6d56c4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984132"
---
# <a name="feature-completeness-recommended-interfaces"></a>Exhaustivité des fonctionnalités : interfaces recommandées

le tableau suivant répertorie les codecs bruts des interfaces WIC (Windows Imaging Component) qui doivent être implémentés.




| Interface | Obligatoire pour | Description | 
|-----------|--------------|-------------|
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a> | Décodeurs | Représente le point de départ pour le décodage d’un fichier image. Fournit l’accès aux propriétés au niveau du conteneur, telles que les miniatures, les frames et la palette.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a> | Décodeurs | Représente un frame d’image spécifique dans le conteneur qui fournit l’accès aux propriétés de niveau image. Il s’agit de l’interface qui décode les bits d’image réels.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> | Décodeurs | Requis pour énumérer et itérer au sein des blocs de métadonnées et appeler les lecteurs de métadonnées appropriés lors de la lecture à partir d’un fichier image. <br /><div class="NOTE"><p>REMARQUE</p><p>Si le format de conteneur brut est compatible TIFF ou utilise des IFD ou IRBs standard pour stocker les métadonnées EXIF ou XMP, les auteurs de codec peuvent choisir d’appeler les lecteurs de métadonnées intégrés plutôt que de les écrire.</p></div> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a> | Décodeurs | Permet à l’appelant de spécifier la mise à l’échelle, le rognage, la rotation ou le format de pixel souhaités pour l’image décodée, ce qui peut améliorer considérablement les performances du décodeur. Par exemple, les décodeurs Microsoft JPEG et le protocole de datagramme sans fil (WDP) utilisent un schéma d’optimisation pyramidal pour accélérer le décodage lorsque la bitmap cible est plus petite que la bitmap source. Windows Vista (et versions ultérieures) tentera d’utiliser cette interface pour extraire une version préliminaire « rapide » d’une image brute chaque fois que la version préliminaire incorporée est manquante ou inférieure à 1 024 pixels dans sa plus grande dimension.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a> | Décodeurs | Requis pour les formats BRUTs. Expose les paramètres qui sont spécifiques au traitement des images BRUTes. Les codecs BRUTs doivent prendre en charge autant de ces paramètres que s’appliquent au codec.<br /> | 
| <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a> | Encodeurs | Représente le point de départ pour l’encodage d’un fichier image. Cette interface est utilisée pour définir les propriétés au niveau du conteneur, telles que les miniatures, les frames et la palette. Il est également nécessaire d’appeler un enregistreur de métadonnées pour activer la persistance des métadonnées dans le fichier image. Pour ces raisons, cette interface est nécessaire même si l’encodage de la bitmap principale au format brut n’est pas pris en charge.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a> | Encodeurs | Représente une image spécifique dans le conteneur. Cette interface est utilisée pour encoder les bits d’image réels et pour définir des métadonnées et des propriétés par image.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> | Encodeurs | Requis pour itérer au sein des blocs de métadonnées et appeler les enregistreurs de métadonnées appropriés lors de la sérialisation d’un fichier image.<br /><div class="NOTE"><p>REMARQUE</p><p>Si le format de conteneur brut est compatible TIFF, les auteurs de codec peuvent choisir d’appeler les enregistreurs de métadonnées intégrés plutôt que de les écrire.</p></div> | 




 

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

 

 




