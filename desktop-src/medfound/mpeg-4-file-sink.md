---
description: Le récepteur de fichiers MPEG-4 crée des fichiers MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Récepteur de fichiers MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106538231"
---
# <a name="mpeg-4-file-sink"></a>Récepteur de fichiers MPEG-4

Le récepteur de fichiers MPEG-4 crée des fichiers MP4. Pour plus d’informations sur le format de fichier MP4, reportez-vous aux documents standard suivants :

-   ISO/IEC 14496-12 : *technologies de l’information--Codage des objets audiovisuels--Partie 12 : format de fichier multimédia de base ISO*
-   ISO/IEC 14496-14 : *technologies de l’information--Codage des objets audiovisuels--Partie 14 : format de fichier MP4*

> [!Note]  
> (Ces ressources peuvent ne pas être disponibles dans certaines langues et certains pays.)

 

Le récepteur de fichiers MPEG-4 n’encapsule pas les fonctionnalités d’encodage.

Pour créer le récepteur de fichiers MPEG-4, appelez la fonction [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) . Le récepteur de fichiers MPEG-4 expose les interfaces suivantes via **QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Zone de description de l’exemple

MP4 est un format de conteneur extensible. La spécification MP4 ne définit pas une structure fixe pour décrire les types de média dans un conteneur MP4. Au lieu de cela, il définit une hiérarchie d’objets qui permet de définir des structures personnalisées pour chaque format. La description du format est stockée dans la zone Description de l’exemple (« STSD ») pour chaque flux. La zone Description de l’exemple contient une liste d’exemples d’entrées. Pour chaque entrée d’exemple, un code de 4 octets, similaire à un code FOURCC, définit la structure de format.

Le récepteur de fichiers MPEG-4 peut générer la zone de description de l’exemple pour les formats suivants :

-   Vidéo H. 264/AVC
-   Audio AAC
-   Audio MP3

Pour les autres formats, la zone Description de l’exemple doit être fournie dans le type de média pour chaque flux. Pour spécifier la zone Description de l’exemple, définissez les attributs suivants sur le type de média :



| Attribut                                                                     | Description                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Exemple de \_ Description du MPEG4 MF MT \_ \_](mf-mt-mpeg4-sample-description.md)      | Contient l’exemple de zone de description en tant qu’objet blob binaire.                                                                                                         |
| [\_Entrée d' \_ exemple \_ de \_ \_ ligne de code MPEG4 MF](mf-mt-mpeg4-current-sample-entry.md) | Spécifie lequel des exemples d’entrées dans la zone Description de l’exemple est actuellement actif. (Facultatif.)<br/> Actuellement, la valeur doit être égale à zéro.<br/> |



 

Dans certains cas, il n’est pas possible de générer un exemple de zone de description tant que toutes les données n’ont pas été encodées. Par exemple, les informations telles que la vitesse de transmission moyenne peuvent ne pas être connues à l’avance. Dans ce cas, vous pouvez mettre à jour le type de média à l’aide de l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sur le récepteur de fichiers MPEG-4. Cette opération doit être effectuée avant la finalisation du récepteur multimédia.

En général, le type de média est créé par un encodeur en amont. L’encodeur peut générer un nouveau type de média pendant la diffusion en continu, via une modification de format dynamique. Pour plus d’informations, consultez [modifications de format dynamique](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>Vidéo H. 264/AVC

Le récepteur de fichiers MPEG-4 prend en charge la version du flux AVC qui possède un flux vidéo élémentaire, avec les paramètres de séquence (SPS) et le jeu de paramètres d’image (PPS) NALUs contenus dans la zone Description de l’exemple, tel que défini dans la section ISO/IEC 14496, partie 15, 5,1. Le récepteur de fichiers ne prend pas en charge l’autre méthode de stockage des NALUs SPS/PPS en tant que flux élémentaire de définition de paramètres distinct.

Le récepteur de fichiers MPEG-4 peut générer la zone de description de l’exemple, mais il doit être fourni avec les NALUs SPS et PPS. Spécifiez ces informations dans le type de média en définissant l’attribut d' [**\_ \_ \_ \_ en-tête de séquence MPEG MF MT**](mf-mt-mpeg-sequence-header-attribute.md) . La valeur de l’attribut est l’en-tête de séquence H. 264. L’en-tête de séquence doit se composer des NALUs SPS et PPS délimités par des codes de démarrage de 3 ou 4 octets.

Si vous le souhaitez, lorsque vous configurez le récepteur de fichiers, vous pouvez omettre l’attribut d' [**\_ \_ \_ \_ en-tête de séquence MPEG MF MT**](mf-mt-mpeg-sequence-header-attribute.md) du type de média initial. Dans ce cas, vous devez mettre à jour le type de média ultérieurement pour inclure l’en-tête de séquence.

Le récepteur de fichiers MPEG-4 présente les exigences suivantes pour les flux de bits AVC :

-   Le flux binaire doit être conforme à la spécification de format d’annexe B H. 264. En particulier, NALUs doit être délimité par des codes de début de 3 ou 4 octets.
-   Les exemples de supports doivent contenir toutes les NALUs de données de secteur et de données qui correspondent à une heure de présentation unique.
-   Lorsque vous écrivez des frames B dans un fichier MP4, vous devez définir à la fois l’horodatage de la présentation et l’horodatage de décodage. Si Stream a un frame B et que l’horodateur de décodage n’est pas défini, l’enregistreur MP4 verra le temps de tramage en arrière et supprimera le frame. 

## <a name="aac-audio"></a>Audio AAC

Pour l’audio AAC, le récepteur de fichiers MPEG-4 peut générer la zone de description de l’exemple pour les sous-types suivants :

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ brut \_ AAC1**

Pour plus d’informations sur ces substypes, consultez [types de média AAC](aac-media-types.md).

Pour le sous-type **MFAudioFormat \_ AAC** , le type de média contient éventuellement l’attribut de [**\_ \_ \_ données utilisateur MF MT User**](mf-mt-user-data-attribute.md) . S’il est présent, cet attribut représente la partie de la structure [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) qui apparaît après la structure **WAVEFORMATEX** (autrement dit, après le membre **wfx** ). Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3. Si l’attribut de **\_ \_ \_ données utilisateur MF MT** n’est pas présent, le flux est supposé être un profil de faible complexité AAC (LC) et le récepteur de fichiers MPEG-4 génère une zone de description d’exemple appropriée.

Pour le sous-type **\_ \_ AAC1 brut MEDIASUBTYPE** , le récepteur multimédia doit contenir l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) et l’attribut doit contenir les données AudioSpecificConfig ().

Le récepteur de fichiers MPEG-4 crée la variante MPEG-4 de la zone de description de l’exemple AAC, à l’aide d’une entrée d’exemple « MP4A » avec objectTypeIndication = 0x40. Elle n’utilise pas les types d’objets MPEG-2.

## <a name="mp3-audio"></a>Audio MP3

Pour le son MP3, le récepteur de fichiers MPEG-4 peut générer la zone de description de l’exemple à partir d’un type de média audio standard. (Voir [types de média audio](audio-media-types.md).)

Le récepteur de fichiers MPEG-4 crée la variante MPEG-4 de la zone de description de l’exemple MP3, à l’aide d’une entrée d’exemple « MP4A » avec objectTypeIndication = 0x6b pour MPEG-1 audio.

## <a name="limitations"></a>Limites

-   La taille maximale du fichier créé est de 4 Go. Dans Windows 8, les fichiers de taille supérieure à 4 GBGB sont pris en charge.
-   Le récepteur de fichiers MPEG-4 ne prend pas en charge les listes de modifications (zones « Edts » et « Elst »).

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Mises à jour de Windows 8 pour la source et le récepteur MPEG-4

-   Prise en charge de la lecture et de l’écriture de rotation ajoutée dans la source et le récepteur MPEG-4 Windows 8. Cela n’est pas pris en charge dans la source et le récepteur Windows 7 MPEG-4.

    La source MPEG-4 lit l’angle de rotation pour une piste vidéo active en tant que somme de l’angle de rotation à partir de’mvhd’et de’tkhd'.

    Le récepteur Microsoft MPEG-4 écrit l’angle de rotation dans’tkhd', mais écrit la matrice de 0 degré (identité) dans’mvhd'. Notez que le récepteur Microsoft MPEG-4 ne prend en charge qu’une seule piste vidéo.

    IPropertyStore lit l’angle de rotation uniquement pour la première piste vidéo en tant que somme de l’angle de rotation à partir de « mvhd » et de « tkhd ».

    IPropertyStore écrit l’angle de rotation uniquement pour la première piste vidéo dans « tkhd » une fois que l’angle de rotation est ajusté en fonction de l’angle de rotation dans « mvhd », s’il existe.

-   Les fragments de film (« moof ») sont pris en charge dans la source et le récepteur MPEG-4 de Windows 8, mais « mfra » n’est pas.
-   H. 263 est pris en charge dans la source MPEG-4 de Windows 8.

    La source MPEG-4 mappe désormais deux FourCC de « H263 » et 263» au format de fichier MPEG-4 sur le type de média de **MFVideoFormat \_ H263**.

-   Plus de prise en charge de FourCC ajoutée pour MJPEG dans la source MPEG-4 Windows 8.

    Le mappage source MPEG-4 foucc de’DMB1 'au type de média de **MFVideoFormat \_ MJPG**.

-   La prise en charge des métadonnées Furigana a été ajoutée dans la source MPEG-4 Windows 8.

    La source MPEG-4 lit les métadonnées Furigana à partir de « SOAL », « décoller », « SOAA », « sonm » et « SOCO ». IPropertyStore lit les métadonnées Furignana à travers l’ensemble des PKEYs correspondantes.

    Le tableau suivant montre le mappage entre le nom canonique de l’interpréteur de commandes, la clé de propriété et l’ID de zone/balise au format de fichier MPEG-4.

    

    | Champ                                | Clé de propriété                         | ID de balise/zone |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. AlbumTitleSortOverride  | AlbumTitleSortOverride de la \_ musique \_  | soal       |
    | System. Music. ArtistSortOverride      | ArtistSortOverride de la \_ musique \_      | soar       |
    | System. Music. AlbumArtistSortOverride | AlbumArtistSortOverride de la \_ musique \_ | soaa       |
    | System. TitleSortOverride             | TitleSortOverride de la \_             | sonm       |
    | System. Music. ComposerSortOverride    | ComposerSortOverride de la \_ musique \_    | soco       |

    

     

-   Prise en charge stéréo 3D Atom ajoutée dans la source MPEG-4 Windows 8.

-   AC3 et DD + prennent en charge ajoutés dans la source et le récepteur MPEG-4 Windows 8.
-   Les fichiers dont la taille est supérieure à 4 Go sont pris en charge dans le récepteur MPEG-4 Windows 8 pour MP4 non fragmenté.
-   Le nettoyage a été optimisé dans la source MPEG-4 de Windows 8.

    Pour réduire la latence, les informations relatives aux deux images clés les plus proches pour une position de recherche particulière sont exposées par le biais de [**IMFSeekInfo :: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Étant donné que l’image clé n’a pas de frames dépendants, elle présente le frame après le décodage d’une seule trame. Utilisez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir cette interface via la source du média, le pipeline ou l’application.

    Définissez rate sur zéro dans la source MPEG-4. Lorsque le pipeline est en mode de nettoyage, le taux est égal à zéro.

-   SPS et PPS peuvent être stockés dans des exemples de données dans un récepteur MPEG-4.

    [MF \_ L' \_ attribut \_ passthrough MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) sur le récepteur MPEG-4 est défini pour permettre l’enregistrement des SP et des PPS avec des exemples d’entrée (données vidéo H. 264). Les clips MP4 générés sont capables d’être lus par la source MPEG-4 de Windows 7 et d’autres.

-   SPS et PPS peuvent être extraits des exemples d’entrée du récepteur MPEG-4.

    Lorsque SPS et PPS ne sont pas définis via l' [ \_ \_ \_ \_ en-tête de séquence MPEG MF MT](mf-mt-mpeg-sequence-header-attribute.md) sur le type de média d’entrée du récepteur MPEG-4, le récepteur MPEG-4 tente d’extraire SPS et PPS des exemples d’entrée. Le récepteur MPEG-4 ignore les exemples d’entrée jusqu’à ce qu’il trouve les premiers SPS et PPS, car tous les exemples d’entrée sans SPS et PPS ne peuvent pas être décodés.

-   les informations 3D dans l’enregistrement de configuration AVC sont prises en charge pour MP4 non fragmenté.
-   La longueur de NALU est exposée pour les exemples compressés H. 264 afin d’optimiser le décodage DXVA H. 264 VLD.

    La source MPEG-4 définit la [ \_ longueur Nalu MF \_ \_ définie](mf-nalu-length-set.md) sur le type de média de sortie de **MFVideoFormat \_ H264 –** ou **MFVideoFormat \_ H264 –**. Il définit l’objet BLOB [des \_ \_ \_ informations de longueur Nalu MF](mf-nalu-length-information.md) sur chaque échantillon de sortie, avec une longueur de Nalu de 4 octets pour différents Nalu dans un échantillon compressé.

-   Ajout de la prise en charge de l’audio MPEG2 ADTS dans la source MP4.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> <dt>

[Récepteurs de médias](media-sinks.md)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
