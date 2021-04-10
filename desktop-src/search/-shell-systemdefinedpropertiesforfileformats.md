---
description: Microsoft Windows fournit un certain nombre de propriétés système que vous pouvez utiliser pour vos formats de fichiers.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Propriétés de System-Defined pour les formats de fichiers personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112402"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>Propriétés de System-Defined pour les formats de fichiers personnalisés

Microsoft Windows fournit un certain nombre de propriétés système que vous pouvez utiliser pour vos formats de fichiers. Si vous créez un format de fichier personnalisé, vous devez prendre en charge autant de propriétés définies par le système que vous le pouvez. Avant de créer un gestionnaire de propriétés personnalisées, vous devez passer en revue les gestionnaires fournis par le système pour déterminer si vous pouvez en utiliser un au lieu d’écrire le vôtre.

Le tableau suivant classe les formats de fichiers, puis répertorie les propriétés système les plus importantes que votre format de fichier doit prendre en charge. Pour offrir une expérience utilisateur optimale, vous devez prendre en charge toutes les propriétés de priorité 1 et 2 pour votre catégorie de format de fichier.

-   [Communications](#communications)
-   [Contacts](#contacts)
-   [Documents](#documents)
-   [Générique](#generic)
-   [Musicale](#music)
-   [Images](#pictures)
-   [Vidéos](#videos)
-   [Rubriques connexes](#related-topics)

## <a name="communications"></a>Communications



| Nom            | Propriété                               | Priority |
|-----------------|----------------------------------------|----------|
| Date de réception   | System. message. DateReceived            | 1        |
| À partir de noms      | System. message. FromName                | 1        |
| Contient des pièces jointes | System. message. HasAttachments          | 1        |
| Mailbox         | System. communication. storeddisplayname | 1        |
| Nom            | System. FileName                        | 1        |
| Objet         | System. Subject                         | 1        |
| En noms        | System. message. ToName                  | 1        |
| Category        | System. Category                        | 2        |
| Type            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contacts



| Nom             | Propriété                           | Priority |
|------------------|------------------------------------|----------|
| Nom du compte     | System. communication. AccountName   | 1        |
| Téléphone professionnel   | System. contact. BusinessTelephone   | 1        |
| Company          | System. Company                     | 1        |
| Adresse de messagerie    | System. contact. PrimaryEmailAddress | 1        |
| importance       | System. ImportanceText              | 1        |
| Téléphone mobile     | System. contact. MobileTelephone     | 1        |
| Adresse professionnelle | System. contact. BusinessAddress     | 2        |
| Télécopie professionnelle     | System. contact. BusinessFaxNumber   | 2        |
| Category         | System. Category                    | 2        |
| Adresse personnelle     | System. contact. HomeAddress         | 2        |
| Téléphone personnel       | System. contact. HomeTelephone       | 2        |
| Intitulé            | System.Title                       | 2        |



 

## <a name="documents"></a>Documents



| Nom      | Propriété             | Priority |
|-----------|----------------------|----------|
| Auteurs   | System.Author        | 1        |
| Texte complet | System. FullText      | 1        |
| Balises      | System.Keywords      | 1        |
| Type      | System.PerceivedType | 1        |
| Category  | System. Category      | 2        |
| Intitulé     | System.Title         | 2        |



 

## <a name="generic"></a>Générique



| Nom     | Propriété             | Priority |
|----------|----------------------|----------|
| Auteurs  | System.Author        | 1        |
| Intitulé    | System.Title         | 1        |
| Type     | System.PerceivedType | 1        |
| Category | System. Category      | 2        |
| Balises     | System.Keywords      | 2        |



 

## <a name="music"></a>Musique



| Nom         | Propriété                     | Priority |
|--------------|------------------------------|----------|
| \#           | System. Music. TrackNumber     | 1        |
| Album        | System. Music. AlbumTitle      | 1        |
| Infographiste      | System. Music. Artist          | 1        |
| Genre        | System. Music. genre           | 1        |
| Rating       | System. Rating                | 1        |
| Intitulé        | System.Title                 | 1        |
| Artiste de l’album | System. Music. AlbumArtist     | 2        |
| Vitesse de transmission     | System. audio. EncodingBitrate | 2        |
| Conductrices   | System. Music. conducteur       | 2        |
| Longueur       | System. Media. Duration        | 2        |
| Protected    | System. DRM. IsProtected       | 2        |
| Year         | System. Media. Year            | 2        |



 

## <a name="pictures"></a>Images



| Nom          | Propriété                        | Priority |
|---------------|---------------------------------|----------|
| Date d’importation | System. DateImported             | 1        |
| Date de prise    | System. photo. DateTaken          | 1        |
| Rating        | System. Rating                   | 1        |
| Balises          | System.Keywords                 | 1        |
| Type          | System.PerceivedType            | 1        |
| Auteurs       | System.Author                   | 2        |
| Fabricant de l’appareil photo  | System. photo. CameraManufacturer | 2        |
| Modèle d’appareil photo  | System. photo. CameraModel        | 2        |
| Commentaires      | System. Comment                  | 2        |
| Dimensions    | System. image. Dimensions         | 2        |



 

## <a name="videos"></a>Vidéos



| Nom         | Propriété                 | Priority |
|--------------|--------------------------|----------|
| Longueur       | System. Media. Duration    | 1        |
| Rating       | System. Rating            | 1        |
| Balises         | System.Keywords          | 1        |
| Type         | System.PerceivedType     | 1        |
| Hauteur du frame | System. Video. FrameHeight | 2        |
| Largeur du cadre  | System. Video. FrameWidth  | 2        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Développement de gestionnaires de propriétés pour Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Système de propriétés](../properties/building-property-handlers.md)
</dt> <dt>

[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
