---
description: le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows Vue d’ensemble du composant de création d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f4276a70b94fd190b7254d8d3d2666581c0c9dbb991dee3ac6e0568b6ee649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772509"
---
# <a name="windows-imaging-component-overview"></a>Windows Vue d’ensemble du composant de création d’images

le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image. WIC permet aux éditeurs de logiciels indépendants et aux fabricants de matériel indépendants (IHV) de développer leurs propres codecs d’image et d’obtenir la même prise en charge de plate-forme que les formats d’images standard (par exemple, TIFF, JPEG, PNG, GIF, BMP et HDPhoto). Un ensemble unique et cohérent d’interfaces est utilisé pour le traitement de tous les images, quel que soit le format d’image, de sorte que toute application utilisant le WIC obtient la prise en charge automatique des nouveaux formats d’image dès l’installation du codec. L’infrastructure de métadonnées extensible permet aux applications de lire et d’écrire leurs propres métadonnées propriétaires directement dans des fichiers image, de sorte que les métadonnées ne sont jamais perdues ou séparées de l’image.

Cette rubrique comprend les sections suivantes.

-   [Windows Fonctionnalités du composant de création d’images](#windows-imaging-component-features)
-   [Codecs natifs](#native-codecs)
-   [Rubriques connexes](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Fonctionnalités du composant de création d’images

Les principales fonctionnalités de WIC sont les suivantes :

-   Permet aux développeurs d’applications d’effectuer des opérations de traitement d’image sur n’importe quel format d’image via un ensemble unique et cohérent d’interfaces courantes, sans avoir besoin d’une connaissance préalable des formats d’image spécifiques.
-   Fournit une architecture « plug-and-Play » extensible pour les codecs d’image, les formats de pixel et les métadonnées, avec la découverte automatique de nouveaux formats au moment de l’exécution.
-   Prend en charge la lecture et l’écriture de métadonnées arbitraires dans les fichiers image, avec la possibilité de conserver les métadonnées non reconnues pendant la modification.
-   Préserve les données d’image de profondeur de bits élevées, jusqu’à 32 bits par canal, dans le pipeline de traitement d’image.
-   Offre une prise en charge intégrée des formats d’image, des formats de pixel et des schémas de métadonnées les plus populaires.

## <a name="native-codecs"></a>Codecs natifs

WIC comprend plusieurs codecs intégrés. Les codecs standard suivants sont fournis avec la plateforme. 

| Codec                                                                                             | Types MIME                       | Décodeurs | Encodeurs |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| bmp (Windows Format Bitmap), bmp Specification v5.                                                | image/bmp                        | Oui      | Oui      |
| GIF (Graphics Interchange format 89a), spécification GIF 89a/89m                                  | image/gif                        | Oui      | Oui      |
| ICO (format d’icône)                                                                                 | image/ico                        | Oui      | Non       |
| JPEG (Joint Photographic Experts Group), spécification d’JFIF 1,02                                  | image/JPEG, image/JPE, image/jpg | Oui      | Oui      |
| PNG (Portable Network Graphics), spécification PNG 1,2                                            | image/png                        | Oui      | Oui      |
| TIFF (Tagged Image File Format), spécification TIFF 6,0                                           | image/TIFF, image/TIF            | Oui      | Oui      |
| Windows Photo multimédia, [spécification de photo HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd. ms-phot                | Oui      | Oui      |
| DDS (surface DirectDraw)                                                                          | image/vnd. ms-DDS                 | Oui      | Oui      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Exemple de CODEC AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
