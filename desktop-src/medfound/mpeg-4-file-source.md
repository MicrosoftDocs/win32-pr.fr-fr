---
description: La source de fichier MPEG-4 analyse les fichiers MP4 et 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Source de fichier MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414056"
---
# <a name="mpeg-4-file-source"></a>Source de fichier MPEG-4

La source de fichier MPEG-4 analyse les fichiers MP4 et 3GPP. Pour plus d’informations sur le format de fichier MP4, reportez-vous aux documents standard suivants :

-   ISO/IEC 14496-12 : *technologies de l’information--Codage des objets audiovisuels--Partie 12 : format de fichier multimédia de base ISO*
-   ISO/IEC 14496-14 : *technologies de l’information--Codage des objets audiovisuels--Partie 14 : format de fichier MP4*

> [!Note]  
> (Ces ressources peuvent ne pas être disponibles dans certaines langues et certains pays.)

 

La source du fichier MPEG-4 ne décode pas les données audio/vidéo dans le fichier.

Cette rubrique contient les sections suivantes :

## <a name="file-extensions-and-mime-types"></a>Extensions de fichier et types MIME

La source du fichier MPEG-4 est la source du média par défaut pour les extensions de nom de fichier suivantes.



| Extension de fichier | Description           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3GP2          | 3GPP2                 |
| .3GPP          | 3GPP                  |
| .m4a           | Audio MPEG-4          |
| .m4v           | Vidéo MPEG-4          |
| .mov           | Film Apple QuickTime |
| .mp4           | MPEG-4 audio ou vidéo |
| . mp4v          | Vidéo MPEG-4          |



 

Il s’agit également de la source du média par défaut pour les types MIME suivants.



| type MIME   | Description  |
|-------------|--------------|
| audio/3GPP  | audio 3GPP   |
| audio/3GPP2 | 3GPP2 audio  |
| Audio/MP4   | Audio MPEG-4 |
| Video/3GPP  | vidéo 3GPP   |
| vidéo/3GPP2 | vidéo 3GPP2  |
| vidéo/MP4   | Vidéo MPEG-4 |



 

## <a name="media-types"></a>Types de médias

MP4 est un format de conteneur extensible. La spécification MP4 ne définit pas une structure fixe pour décrire les types de média dans un conteneur MP4. Au lieu de cela, il définit une hiérarchie d’objets qui permet de définir des structures personnalisées pour chaque format. La description du format est stockée dans la zone Description de l’exemple (« STSD ») pour ce flux. La zone Description de l’exemple contient une liste d’exemples d’entrées. Pour chaque entrée d’exemple, un code de 4 octets, similaire à un code FOURCC, définit la structure de format.

Cette extensibilité signifie que la source du fichier MPEG-4 ne peut pas reconnaître toutes les descriptions de format possibles. Au lieu de cela, il prend une approche à deux niveaux lors de la création de types de média pour les flux. Au minimum, chaque type de média contient les attributs suivants.



| Attribut                                                                     | Description                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                     | Égal à **MFMediaType \_ audio** ou **MFMediaType \_ vidéo**.     |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                            | Spécifie le sous-type de flux.                                  |
| [\_Exemple de \_ Description du MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Contient la zone de description complète de l’exemple en tant qu’objet blob binaire. |
| [\_Entrée d' \_ exemple \_ de \_ \_ ligne de code MPEG4 MF](mf-mt-mpeg4-current-sample-entry.md) | Spécifie l’entrée actuelle dans la zone Description de l’exemple.     |



 

La source de fichier MPEG-4 reconnaît des exemples de types d’entrée. Pour ces entrées, il peut analyser la structure du format et créer un type de média complet, avec des attributs supplémentaires qui décrivent les détails du format. Consultez [attributs de type de média](media-type-attributes.md).

La source de fichier MPEG-4 peut analyser les exemples d’entrées suivants.



| Exemple de code d’entrée | Type principal | Subtype                                                               | Description                                         | Notes                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alaw            | Audio      | **\_alaw format \_ Wave**                                                | Codage de la Loi                                        |                                                                                                                                                                                                  |
| gif            | Vidéo      | **MFVideoFormat \_ MJPG**                                               | Flux photo-JPEG                                   | Le format de conteneur QuickTime prend également en charge les flux Motion JPEG avec les entrées « mjpa » ou « MJPB », mais la source du fichier MPEG-4 ne fournit pas de type de média complet pour ces types.               |
| 'avc1'            | Vidéo      | **MFVideoFormat \_ H264 –**                                               | Vidéo H. 264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **\_Mp3 MFAudioFormat**<br/>   | AAC ou MP3                                          | L’entrée « MP4A » peut décrire d’autres formats audio MPEG, mais la source du fichier MPEG-4 n’analyse pas la structure du format.                                                                          |
| mp4v            | Vidéo      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ mp4v**<br/> | MPEG-4 partie 2                                       | **MFVideoFormat \_ M4S2** est utilisé pour le profil simple MPEG-4 part 2.<br/> **MFVideoFormat \_ MP4V** est utilisé pour tous les autres profils MPEG-4 part 2, y compris le profil Advanced simple.<br/> |
| première            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM 8 bits                                     |                                                                                                                                                                                                  |
| 'sowt'            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM Little-endian 16 bits                      |                                                                                                                                                                                                  |
| complément            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM 16 bits Big-endian                         | La source de fichier MPEG-4 convertit les données audio au format Little endian.                                                                                                                          |
| ulaw            | Audio      | **\_Mulaw format \_ Wave**                                               | μ-codage de la Loi                                        |                                                                                                                                                                                                  |
| 'VC-1 '            | Vidéo      | **MFVideoFormat \_ WVC1**                                               | Vidéo VC-1                                          |                                                                                                                                                                                                  |
| None            | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM 8 bits ou 16 bits Big-endian                | La source de fichier MPEG-4 convertit les données audio au format Little endian.                                                                                                                          |
| 0x00000000        | Audio      | **\_PCM MFAudioFormat**                                                | audio PCM 8 bits ou 16 bits Big-endian                | La source de fichier MPEG-4 convertit les données audio au format Little endian.                                                                                                                          |
| 0x6d730002        | Audio      | **\_format Wave \_ ADPCM**                                               | Modulation de code par impulsion différentielle adaptative (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **\_format Wave \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

Pour tous les autres codes non répertoriés dans le tableau précédent, la source du fichier MPEG-4 définit le sous-type comme suit :

1.  *sous-type* = MFMPEG4Format \_ base
2.  *sous-type*. Data1 = exemple de code d’entrée

Pour les codes non affichés dans le tableau, un décodeur doit utiliser l’exemple de description de l' [ \_ exemple de \_ \_ \_ Description du MPEG4 MF MT](mf-mt-mpeg4-sample-description.md) pour analyser la zone de description de l’exemple.

Pour obtenir la liste des exemples de codes d’entrée et des liens vers des spécifications pertinentes, consultez le site Web de l' [autorité d’inscription « MP4 »](https://mp4ra.org) .

## <a name="limitations"></a>Limites

La source du fichier MPEG-4 ne prend pas en charge les fonctionnalités suivantes des fichiers MP4 :

-   Pistes externes.
-   Fragments de film (zones « moof » ou « mfra »). « moof » est pris en charge dans Windows 8.
-   Présentations diffusées en continu. La source de fichier MPEG-4 ignore les pistes d’indication en mode silencieux.
-   Recherche par code de temps SMPTE.
-   Atomes compressés ('CMOV').

Seuls les flux vidéo et audio sont pris en charge. Toutes les pistes qui contiennent d’autres types de flux sont ignorées silencieusement. Les données multimédias doivent être placées à l’intérieur des atomes « MDAT ».

si la mise à jour du supplément Platform pour Windows vista est installée, la source du fichier MPEG-4 est disponible sur Windows vista, mais n’est accessible sur Windows vista qu’à l’aide du [lecteur source](source-reader.md).

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 les mises à jour de la source et du récepteur MPEG-4

-   prise en charge de la lecture et de l’écriture de Rotation ajoutée dans Windows 8 source et le récepteur MPEG-4. cela n’est pas pris en charge dans la source et le récepteur Windows 7 MPEG-4.

    La source MPEG-4 lit l’angle de rotation pour une piste vidéo active en tant que somme de l’angle de rotation à partir de’mvhd’et de’tkhd'.

    Le récepteur Microsoft MPEG-4 écrit l’angle de rotation dans’tkhd', mais écrit la matrice de 0 degré (identité) dans’mvhd'. Notez que le récepteur Microsoft MPEG-4 ne prend en charge qu’une seule piste vidéo.

    IPropertyStore lit l’angle de rotation uniquement pour la première piste vidéo en tant que somme de l’angle de rotation à partir de « mvhd » et de « tkhd ».

    IPropertyStore écrit l’angle de rotation uniquement pour la première piste vidéo dans « tkhd » une fois que l’angle de rotation est ajusté en fonction de l’angle de rotation dans « mvhd », s’il existe.

-   les fragments de film (« moof ») sont pris en charge dans Windows 8 source et le récepteur MPEG-4, mais « mfra » n’est pas.
-   H. 263 est pris en charge dans Windows 8 source MPEG-4.

    La source MPEG-4 mappe désormais deux FourCC de « H263 » et 263» au format de fichier MPEG-4 sur le type de média de **MFVideoFormat \_ H263**.

-   plus de prise en charge de fourcc ajoutée pour MJPEG dans Windows 8 source MPEG-4.

    Le mappage source MPEG-4 foucc de’DMB1 'au type de média de **MFVideoFormat \_ MJPG**.

-   prise en charge des métadonnées Furigana ajoutées dans Windows 8 source MPEG-4.

    La source MPEG-4 lit les métadonnées Furigana à partir de « SOAL », « décoller », « SOAA », « sonm » et « SOCO ». IPropertyStore lit les métadonnées Furignana à travers l’ensemble des PKEYs correspondantes.

    Le tableau suivant montre le mappage entre le nom canonique de l’interpréteur de commandes, la clé de propriété et l’ID de zone/balise au format de fichier MPEG-4.

    

    | Champ                                | Clé de propriété                         | ID de balise/zone |
    |--------------------------------------|--------------------------------------|------------|
    | Requise. Musique. AlbumTitleSortOverride  | Musique de la \_ \_ AlbumTitleSortOverride  | soal       |
    | Requise. Musique. ArtistSortOverride      | Musique de la \_ \_ ArtistSortOverride      | Tu       |
    | Requise. Musique. AlbumArtistSortOverride | Musique de la \_ \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | TitleSortOverride de la \_             | sonm       |
    | Requise. Musique. ComposerSortOverride    | Musique de la \_ \_ ComposerSortOverride    | soco       |

    

     

-   prise en charge stéréo 3d atom ajoutée dans Windows 8 source MPEG-4.

-   AC3 et DD + prennent en charge ajoutés dans Windows 8 source et le récepteur MPEG-4.
-   les fichiers dont la taille est supérieure à 4 gigaoctets (go) sont pris en charge dans Windows 8 récepteur MPEG-4 pour MP4 non fragmenté.
-   le nettoyage a été optimisé dans Windows 8 source MPEG-4.

    Pour réduire la latence, les informations relatives aux deux images clés les plus proches pour une position de recherche particulière sont exposées par le biais de [**IMFSeekInfo :: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Étant donné que l’image clé n’a pas de frames dépendants, elle présente le frame après le décodage d’une seule trame. Utilisez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir cette interface via la source du média, le pipeline ou l’application.

    Définissez rate sur zéro dans la source MPEG-4. Lorsque le pipeline est en mode de nettoyage, le taux est égal à zéro.

-   SPS et PPS peuvent être stockés dans des exemples de données dans un récepteur MPEG-4.

    [MF \_ L' \_ attribut \_ passthrough MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) sur le récepteur MPEG-4 est défini pour permettre l’enregistrement des SP et des PPS avec des exemples d’entrée (données vidéo H. 264). les clips mp4 générés sont en mesure de lire Windows 7 MPEG-4 source et d’autres.

-   SPS et PPS peuvent être extraits des exemples d’entrée du récepteur MPEG-4.

    Lorsque SPS et PPS ne sont pas définis via l' [ \_ \_ \_ \_ en-tête de séquence MPEG MF MT](mf-mt-mpeg-sequence-header-attribute.md) sur le type de média d’entrée du récepteur MPEG-4, le récepteur MPEG-4 tente d’extraire SPS et PPS des exemples d’entrée. Le récepteur MPEG-4 ignore les exemples d’entrée jusqu’à ce qu’il trouve les premiers SPS et PPS, car tous les exemples d’entrée sans SPS et PPS ne peuvent pas être décodés.

-   les informations 3D dans l’enregistrement de configuration AVC sont prises en charge pour MP4 non fragmenté.
-   La longueur de NALU est exposée pour les exemples compressés H. 264 afin d’optimiser le décodage DXVA H. 264 VLD.

    La source MPEG-4 définit la [ \_ longueur Nalu MF \_ \_ définie](mf-nalu-length-set.md) sur le type de média de sortie de **MFVideoFormat \_ H264 –** ou **MFVideoFormat \_ H264 –**. Il définit l’objet BLOB [des \_ \_ \_ informations de longueur Nalu MF](mf-nalu-length-information.md) sur chaque échantillon de sortie, avec une longueur de Nalu de 4 octets pour différents Nalu dans un échantillon compressé.

-   Ajout de la prise en charge de l’audio MPEG2 ADTS dans la source MP4.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




