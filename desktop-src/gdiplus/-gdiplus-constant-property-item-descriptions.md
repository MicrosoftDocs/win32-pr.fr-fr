---
description: La liste suivante fournit des descriptions des éléments de propriété pris en charge par Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descriptions des éléments de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636121"
---
# <a name="property-item-descriptions"></a>Descriptions des éléments de propriété

La liste suivante fournit des descriptions des éléments de propriété pris en charge par Windows GDI+. Les descriptions sont courtes et générales afin qu’elles s’appliquent à un large éventail de formats de fichiers image. Pour obtenir une description détaillée de la façon dont un élément de propriété est utilisé par un format de fichier particulier, consultez la spécification de ce format de fichier. Pour obtenir des liens vers plusieurs spécifications de fichier et d’autres documents qui décrivent les métadonnées en détail, consultez [spécifications de format de fichier image](-gdiplus-constant-image-file-format-specifications.md).

Le format EXIF (Exchangeable Image File) est une norme JEIDA (Japon Electronic Development Association), révisée le 1998 juin en version 2,1. Des parties de la spécification EXIF sont utilisées avec l’autorisation JEIDA.

## <a name="propertytaggpsver"></a>PropertyTagGpsVer

Version de l’IFD du système de positionnement global (GPS), donnée sous la forme 2.0.0.0. Cette balise est obligatoire lorsque la balise PropertyTagGpsIFD est présente. Lorsque la version est 2.0.0.0, la valeur de la balise est 0x02000000.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0000              |
| Type  | PropertyTagTypeByte |
| Nombre | 4                   |



 

## <a name="propertytaggpslatituderef"></a>PropertyTagGpsLatitudeRef

Chaîne de caractères se terminant par un caractère null qui spécifie si la latitude est le Nord ou le sud. `N` spécifie la latitude nord et `S` spécifie la latitude sud.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0001                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpslatitude"></a>PropertyTagGpsLatitude

Latitude. La latitude est exprimée sous la forme de trois valeurs rationnelles donnant respectivement les degrés, les minutes et les secondes. Lorsque les degrés, les minutes et les secondes sont exprimés, le format est JJ/1, mm/1, SS/1. Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est JJ/1, mmmm/100, 0/1.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0002                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytaggpslongituderef"></a>PropertyTagGpsLongitudeRef

Chaîne de caractères se terminant par un caractère null qui spécifie si la longitude est ou longitude ouest. `E` spécifie la longitude est et `W` spécifie la longitude ouest.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0003                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpslongitude"></a>PropertyTagGpsLongitude

Longitude. La longitude est exprimée sous la forme de trois valeurs rationnelles accordant respectivement les degrés, les minutes et les secondes. Lorsque les degrés, les minutes et les secondes sont exprimés, le format est DDD/1, mm/1, SS/1. Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est DDD/1, mmmm/100, 0/1.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0004                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>PropertyTagGpsAltitudeRef

Altitude de référence, en mètres.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0005              |
| Type  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytaggpsaltitude"></a>PropertyTagGpsAltitude

Altitude, en mètres, en fonction de l’altitude de référence spécifiée par PropertyTagGpsAltitudeRef.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0006                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsgpstime"></a>PropertyTagGpsGpsTime

Heure au format UTC (temps universel coordonné). La valeur est exprimée sous la forme de trois nombres rationnels qui donnent l’heure, la minute et la seconde.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0007                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>PropertyTagGpsGpsSatellites

Chaîne de caractères se terminant par un caractère null qui spécifie les satellites GPS utilisés pour les mesures. Cette balise peut être utilisée pour spécifier le numéro d’identification, l’angle d’élévation, l’azimut, le SNR et d’autres informations sur chaque satellite. Le format n’est pas spécifié. Si le récepteur GPS n’est pas en mesure de prendre des mesures, la valeur de la balise doit être définie sur **null**.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0008                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytaggpsgpsstatus"></a>PropertyTagGpsGpsStatus

Chaîne de caractères se terminant par un caractère null qui spécifie l’état du récepteur GPS lorsque l’image est enregistrée. `A` signifie que la mesure est en cours et `V` signifie que la mesure est l’interopérabilité.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0009                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsgpsmeasuremode"></a>PropertyTagGpsGpsMeasureMode

Chaîne de caractères se terminant par un caractère null qui spécifie le mode de mesure GPS. `2` spécifie la mesure 2D et `3` spécifie une mesure 3D.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x000A                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsgpsdop"></a>PropertyTagGpsGpsDop

GPS DOP (degré de précision des données). Une valeur HDOP est écrite en cours de mesure 2D, et une valeur PDOP est écrite en cours de mesure 3D.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x000B                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsspeedref"></a>PropertyTagGpsSpeedRef

Chaîne de caractères se terminant par un caractère null qui spécifie l’unité utilisée pour exprimer la vitesse de déplacement du récepteur GPS. `K`, `M` et `N` représentent des kilomètres par heure, miles par heure et nœuds respectivement.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x000C                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsspeed"></a>PropertyTagGpsSpeed

Vitesse du déplacement du récepteur GPS.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x000D                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpstrackref"></a>PropertyTagGpsTrackRef

Chaîne de caractères se terminant par un caractère null qui spécifie la référence pour donner la direction du mouvement du récepteur GPS. `T` spécifie la direction réelle et `M` spécifie la direction magnétique.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x000E                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpstrack"></a>PropertyTagGpsTrack

Direction du mouvement du récepteur GPS. La plage de valeurs est comprise entre 0,00 et 359,99.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x000F                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>PropertyTagGpsImgDirRef

Chaîne de caractères se terminant par un caractère null qui spécifie la référence pour la direction de l’image lorsqu’elle est capturée. `T` spécifie la direction réelle et `M` spécifie la direction magnétique.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0010                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsimgdir"></a>PropertyTagGpsImgDir

Direction de l’image lors de sa capture. La plage de valeurs est comprise entre 0,00 et 359,99.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0011                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>PropertyTagGpsMapDatum

Chaîne de caractères se terminant par un caractère null qui spécifie les données d’enquête géodésique utilisées par le récepteur GPS. Si les données de l’enquête sont limitées au Japon, la valeur de cette balise est `TOKYO` ou `WGS-84` .



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0012                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytaggpsdestlatref"></a>PropertyTagGpsDestLatRef

Chaîne de caractères se terminant par un caractère null qui spécifie si la latitude du point de destination est la latitude nord ou sud. `N` spécifie la latitude nord et `S` spécifie la latitude sud.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0013                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsdestlat"></a>PropertyTagGpsDestLat

Latitude du point de destination. La latitude est exprimée sous la forme de trois valeurs rationnelles donnant respectivement les degrés, les minutes et les secondes. Lorsque les degrés, les minutes et les secondes sont exprimés, le format est JJ/1, mm/1, SS/1. Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est JJ/1, mmmm/100, 0/1.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0014                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>PropertyTagGpsDestLongRef

Chaîne de caractères terminée par le caractère null qui spécifie si la longitude du point de destination est l’est ou la longitude ouest. `E` spécifie la longitude est et `W` spécifie la longitude ouest.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0015                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsdestlong"></a>PropertyTagGpsDestLong

Longitude du point de destination. La longitude est exprimée sous la forme de trois valeurs rationnelles accordant respectivement les degrés, les minutes et les secondes. Lorsque les degrés, les minutes et les secondes sont exprimés, le format est DDD/1, mm/1, SS/1. Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est DDD/1, mmmm/100, 0/1.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0016                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>PropertyTagGpsDestBearRef

Chaîne de caractères se terminant par un caractère null qui spécifie la référence utilisée pour donner le palier au point de destination. `T` spécifie la direction réelle et `M` spécifie la direction magnétique.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0017                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsdestbear"></a>PropertyTagGpsDestBear

Palier au point de destination. La plage de valeurs est comprise entre 0,00 et 359,99.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0018                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>PropertyTagGpsDestDistRef

Chaîne de caractères se terminant par un caractère null qui spécifie l’unité utilisée pour exprimer la distance au point de destination. K, M et N représentent les kilomètres, les miles et les nœuds, respectivement.



| Informations sur la propriété | Value |
|-------|--------------------------------------------|
| Tag   | 0x0019                                     |
| Type  | PropertyTagTypeASCII                       |
| Nombre | 2 (un caractère plus la marque de fin NULL) |



 

## <a name="propertytaggpsdestdist"></a>PropertyTagGpsDestDist

Distance au point de destination.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x001A                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>PropertyTagNewSubfileType

Type de données dans un sous-fichier.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x00FE              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagsubfiletype"></a>PropertyTagSubfileType

Type de données dans un sous-fichier.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x00FF               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

Nombre de pixels par ligne.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0100                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagimageheight"></a>PropertyTagImageHeight

Nombre de lignes de pixels.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0101                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagbitspersample"></a>PropertyTagBitsPerSample

Nombre de bits par composant de couleur. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0102                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagcompression"></a>PropertyTagCompression

Schéma de compression utilisé pour les données de l’image.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0103               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagphotometricinterp"></a>PropertyTagPhotometricInterp

Comment les données de pixels seront interprétées.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0106               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthreshholding"></a>PropertyTagThreshHolding

Technique utilisée pour convertir des pixels gris en pixels noirs et blancs.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0107               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellwidth"></a>PropertyTagCellWidth

Largeur de la matrice de trame ou de trame.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0108               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellheight"></a>PropertyTagCellHeight

Hauteur de la matrice de tramage ou de simili.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0109               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagfillorder"></a>PropertyTagFillOrder

Ordre logique des bits dans un octet.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x010A               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdocumentname"></a>PropertyTagDocumentName

Chaîne de caractères se terminant par un caractère null qui spécifie le nom du document à partir duquel l’image a été analysée.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x010D                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagimagedescription"></a>PropertyTagImageDescription

Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x010E                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagequipmake"></a>PropertyTagEquipMake

Chaîne de caractères se terminant par un caractère null qui spécifie le fabricant de l’équipement utilisé pour enregistrer l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x010F                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagequipmodel"></a>PropertyTagEquipModel

Chaîne de caractères se terminant par un caractère null qui spécifie le nom du modèle ou le numéro de modèle de l’équipement utilisé pour enregistrer l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0110                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagstripoffsets"></a>PropertyTagStripOffsets

Pour chaque bande, le décalage d’octet de cette bande. Voir aussi [PropertyTagRowsPerStrip](#propertytagrowsperstrip) et [PropertyTagStripBytesCount](#propertytagstripbytescount).



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0111                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Nombre | Nombre de bandes                            |



 

## <a name="propertytagorientation"></a>PropertyTagOrientation

Orientation de l’image affichée en termes de lignes et de colonnes.



Tag

0x0112

Type

PropertyTagTypeShort

Count

1

1-la ligne 0 est en haut de l’image visuelle et la colonne 0 est le côté gauche du visuel. 2-la ligne 0 est en haut de l’image et la colonne 0 est le côté droit visuel. 3-la ligne 0 est au bas du visuel de l’image et la colonne 0 est le côté droit visuel. 4-la ligne 0 est au bas du visuel de l’image et la colonne 0 est le côté gauche du visuel. 5-la ligne 0 est le côté gauche de l’image et la colonne 0 est la partie supérieure du visuel. 6-la ligne 0 est le côté droit de l’image et la colonne 0 est la partie supérieure du visuel. 7-la ligne 0 est le côté droit de l’image et la colonne 0 est le bas du visuel. 8-la ligne 0 est le côté gauche de l’image et la colonne 0 est le bas du visuel.



 

## <a name="propertytagsamplesperpixel"></a>PropertyTagSamplesPerPixel

Nombre de composants de couleur par pixel.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0115               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrowsperstrip"></a>PropertyTagRowsPerStrip

Nombre de lignes par bande. Voir aussi [PropertyTagStripBytesCount](#propertytagstripbytescount) et [PropertyTagStripOffsets](#propertytagstripoffsets).



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0116                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagstripbytescount"></a>PropertyTagStripBytesCount

Pour chaque bande, nombre total d’octets dans cette bande.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0117                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Nombre | Nombre de bandes                            |



 

## <a name="propertytagminsamplevalue"></a>PropertyTagMinSampleValue

Pour chaque composant de couleur, valeur minimale assignée à ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0118                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagmaxsamplevalue"></a>PropertyTagMaxSampleValue

Pour chaque composant de couleur, valeur maximale affectée à ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0119                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagxresolution"></a>PropertyTagXResolution

Nombre de pixels par unité dans la direction de la largeur de l’image (x). L’unité est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x011A                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyresolution"></a>PropertyTagYResolution

Nombre de pixels par unité dans la direction de la hauteur d’image (y). L’unité est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x011B                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagplanarconfig"></a>PropertyTagPlanarConfig

Si les composants de pixel sont enregistrés au format de forme groupée ou planaire.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x011C               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagpagename"></a>PropertyTagPageName

Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la page à partir de laquelle l’image a été analysée.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x011D                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagxposition"></a>PropertyTagXPosition

Décalage du côté gauche de la page vers le côté gauche de l’image. L’unité de mesure est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x011E                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyposition"></a>PropertyTagYPosition

Décalage à partir du haut de la page vers le haut de l’image. L’unité de mesure est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x011F                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagfreeoffset"></a>PropertyTagFreeOffset

Pour chaque chaîne d’octets inutilisés contigus, il s’agit du décalage d’octet de cette chaîne.



| Informations sur la propriété | Value |
|------|---------------------|
| Tag  | 0x0120              |
| Type | PropertyTagTypeLong |



 

## <a name="propertytagfreebytecounts"></a>PropertyTagFreeByteCounts

Pour chaque chaîne d’octets inutilisés contigus, nombre d’octets dans cette chaîne.



| Informations sur la propriété | Value |
|-------|-----------------------------------------------|
| Tag   | 0x0121                                        |
| Type  | PropertyTagTypeLong                           |
| Nombre | Nombre de chaînes d’octets inutilisés contigus. |



 

## <a name="propertytaggrayresponseunit"></a>PropertyTagGrayResponseUnit

Précision du nombre spécifié par PropertyTagGrayResponseCurve. 1 spécifie dixièmes, 2 spécifie centièmes, 3 spécifie des millièmes, et ainsi de suite.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0122               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>PropertyTagGrayResponseCurve

Pour chaque valeur de pixel possible dans une image en nuances de gris, la densité optique de cette valeur de pixel.



| Informations sur la propriété | Value |
|-------|---------------------------------|
| Tag   | 0x0123                          |
| Type  | PropertyTagTypeShort            |
| Nombre | Nombre de valeurs de pixel possibles |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

Ensemble d’indicateurs liés à l’encodage T4.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0124              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

Ensemble d’indicateurs associés à l’encodage T6.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0125              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagresolutionunit"></a>PropertyTagResolutionUnit

Unité de mesure pour la résolution horizontale et la résolution verticale.



Tag

0x0128

Type

PropertyTagTypeShort

Count

1

2 pouces, 3-centimètres



 

## <a name="propertytagpagenumber"></a>PropertyTagPageNumber

Numéro de page de la page à partir de laquelle l’image a été numérisée.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0129               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagtransferfunction"></a>PropertyTagTransferFunction

Tables qui spécifient des fonctions de transfert pour l’image.



| Informations sur la propriété | Value |
|-------|------------------------------------------------------|
| Tag   | 0x012D                                               |
| Type  | PropertyTagTypeShort                                 |
| Nombre | Nombre total de mots de 16 bits requis pour les tables |



 

## <a name="propertytagsoftwareused"></a>PropertyTagSoftwareUsed

Chaîne de caractères se terminant par un caractère null qui spécifie le nom et la version du logiciel ou du microprogramme de l’appareil utilisé pour générer l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0131                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagdatetime"></a>PropertyTagDateTime

Date et heure de création de l’image.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0132               |
| Type  | PropertyTagTypeASCII |
| Nombre | 20                   |



 

## <a name="propertytagartist"></a>PropertyTagArtist

Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la personne qui a créé l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x013B                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytaghostcomputer"></a>PropertyTagHostComputer

Chaîne de caractères se terminant par un caractère null qui spécifie l’ordinateur et/ou le système d’exploitation utilisé pour créer l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x013C                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagpredictor"></a>PropertyTagPredictor

Type de schéma de prédiction appliqué aux données de l’image avant l’application du schéma d’encodage.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x013D               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagwhitepoint"></a>PropertyTagWhitePoint

Chromatique du point blanc de l’image.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x013E                  |
| Type  | PropertyTagTypeRational |
| Nombre | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>PropertyTagPrimaryChromaticities

Pour chacune des trois couleurs primaires dans l’image, la chromatique de cette couleur.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x013F                  |
| Type  | PropertyTagTypeRational |
| Nombre | 6                       |



 

## <a name="propertytagcolormap"></a>PropertyTagColorMap

Palette de couleurs (table de choix) pour une image indexée par palette.



| Informations sur la propriété | Value |
|-------|-------------------------------------------------|
| Tag   | 0x0140                                          |
| Type  | PropertyTagTypeShort                            |
| Nombre | Nombre de mots de 16 bits requis pour la palette |



 

## <a name="propertytaghalftonehints"></a>PropertyTagHalftoneHints

Informations utilisées par la fonction de demi-teinte



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0141               |
| Type  | PropertyTagTypeShort |
| Nombre | 2                    |



 

## <a name="propertytagtilewidth"></a>PropertyTagTileWidth

Nombre de colonnes de pixels dans chaque vignette.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0142                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtilelength"></a>PropertyTagTileLength

Nombre de lignes de pixels dans chaque vignette.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0143                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtileoffset"></a>PropertyTagTileOffset

Pour chaque vignette, le décalage d’octet de cette vignette.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0144              |
| Type  | PropertyTagTypeLong |
| Nombre | Nombre de vignettes     |



 

## <a name="propertytagtilebytecounts"></a>PropertyTagTileByteCounts

Pour chaque vignette, nombre d’octets dans cette vignette.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0145                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Nombre | Nombre de vignettes                             |



 

## <a name="propertytaginkset"></a>PropertyTagInkSet

Jeu d’encres utilisé dans une image séparée.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x014C               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaginknames"></a>PropertyTagInkNames

Séquence de chaînes de caractères concaténées, se terminant par un caractère null, qui spécifient les noms des encres utilisées dans une image séparée.



| Informations sur la propriété | Value |
|-------|------------------------------------------------------------------------|
| Tag   | 0x014D                                                                 |
| Type  | PropertyTagTypeASCII                                                   |
| Nombre | Longueur totale de la séquence de chaînes, y compris les marques de fin NULL |



 

## <a name="propertytagnumberofinks"></a>PropertyTagNumberOfInks

Nombre d’encres.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x014E               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdotrange"></a>PropertyTagDotRange

Valeurs de composant de couleur qui correspondent à un point de 0 pour cent et un point de 100 pour cent.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x0150                                      |
| Type  | PropertyTagTypeByte ou PropertyTagTypeShort |
| Nombre | 2 ou 2 × PropertyTagSamplesPerPixel           |



 

## <a name="propertytagtargetprinter"></a>PropertyTagTargetPrinter

Chaîne de caractères se terminant par un caractère null qui décrit l’environnement d’impression prévu.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0151                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagextrasamples"></a>PropertyTagExtraSamples

Nombre de composants de couleur supplémentaires. Par exemple, un composant supplémentaire peut contenir une valeur alpha.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0152               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagsampleformat"></a>PropertyTagSampleFormat

Pour chaque composant de couleur, le format numérique (non signé, signé, à virgule flottante) de ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0153                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagsminsamplevalue"></a>PropertyTagSMinSampleValue

Pour chaque composant de couleur, valeur minimale de ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|-----------------------------------------------------|
| Tag   | 0x0154                                              |
| Type  | Type qui correspond le mieux aux données du composant pixel |
| Nombre | Nombre d’échantillons (composants) par pixel            |



 

## <a name="propertytagsmaxsamplevalue"></a>PropertyTagSMaxSampleValue

Pour chaque composant de couleur, valeur maximale de ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|-----------------------------------------------------|
| Tag   | 0x0155                                              |
| Type  | Type qui correspond le mieux aux données du composant pixel |
| Nombre | Nombre d’échantillons (composants) par pixel            |



 

## <a name="propertytagtransferrange"></a>PropertyTagTransferRange

Table de valeurs qui étend la plage de la fonction de transfert.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0156               |
| Type  | PropertyTagTypeShort |
| Nombre | 6                    |



 

## <a name="propertytagjpegproc"></a>PropertyTagJPEGProc

Processus de compression JPEG.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0200               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeginterformat"></a>PropertyTagJPEGInterFormat

Décalage au début d’un flux binaire JPEG.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0201              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpeginterlength"></a>PropertyTagJPEGInterLength

Longueur, en octets, du flux binaire JPEG.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x0202              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>PropertyTagJPEGRestartInterval

Longueur de l’intervalle de redémarrage.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0203               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>PropertyTagJPEGLosslessPredictors

Pour chaque composant de couleur, il s’agit d’une valeur de sélection de prédiction sans perte pour ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0205                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagjpegpointtransforms"></a>PropertyTagJPEGPointTransforms

Pour chaque composant de couleur, valeur de transformation de point pour ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0206                                   |
| Type  | PropertyTagTypeShort                     |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagjpegqtables"></a>PropertyTagJPEGQTables

Pour chaque composant de couleur, décalage vers la table de quantification pour ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0207                                   |
| Type  | PropertyTagTypeLong                      |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagjpegdctables"></a>PropertyTagJPEGDCTables

Pour chaque composant de couleur, décalage vers la table de Huffman de contrôle de l’élément de contrôle (ou table de Huffman sans perte) pour ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0208                                   |
| Type  | PropertyTagTypeLong                      |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagjpegactables"></a>PropertyTagJPEGACTables

Pour chaque composant de couleur, décalage vers la table de Huffman AC pour ce composant. Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informations sur la propriété | Value |
|-------|------------------------------------------|
| Tag   | 0x0209                                   |
| Type  | PropertyTagTypeLong                      |
| Nombre | Nombre d’échantillons (composants) par pixel |



 

## <a name="propertytagycbcrcoefficients"></a>PropertyTagYCbCrCoefficients

Coefficients pour la transformation des données d’image RVB en données d’image YCbCr.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0211                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>PropertyTagYCbCrSubsampling

Taux d’échantillonnage des composants de chrominance par rapport au composant luminance.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0212               |
| Type  | PropertyTagTypeShort |
| Nombre | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>PropertyTagYCbCrPositioning

Position des composants de chrominance par rapport au composant luminance.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x0213               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrefblackwhite"></a>PropertyTagREFBlackWhite

Valeur du point noir de référence et valeur du point blanc de référence.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0214                  |
| Type  | PropertyTagTypeRational |
| Nombre | 6                       |



 

## <a name="propertytaggamma"></a>PropertyTagGamma

Valeur gamma attachée à l’image. La valeur gamma est stockée sous la forme d’un nombre rationnel (paire de **long**) avec un numérateur de 100000. Par exemple, la valeur gamma 2,2 est stockée en tant que paire (100000, 45455).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x0301                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>PropertyTagICCProfileDescriptor

Chaîne de caractères se terminant par un caractère null qui identifie un profil ICC.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0302                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagsrgbrenderingintent"></a>PropertyTagSRGBRenderingIntent

Comment l’image doit être affichée comme défini par le consortium de couleur international (ICC). Si un objet  [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ est construit avec le paramètre *UseEmbeddedColorManagement* défini sur **true**, GDI+ effectue le rendu de l’image en fonction de l’intention de rendu spécifiée. L’intention peut être définie sur perception, Colorimétrie relative, saturation ou Colorimétrie absolue.

-   L’intention de perception, adaptée aux photographies, offre une bonne adaptation à la gamme d’appareils d’affichage au détriment de la précision colorimétrique.
-   L’intention de Colorimétrie relative convient pour les images (par exemple, des logos) qui requièrent une correspondance d’apparence de couleur par rapport au point blanc de l’appareil d’affichage.
-   L’objectif de saturation, qui convient aux graphiques et aux graphiques, conserve la saturation aux dépens de la teinte et de la luminosité.
-   L’intention de Colorimétrie absolue est adaptée aux épreuves (aperçus d’images destinées à un autre périphérique d’affichage) qui nécessitent la préservation de la colorimétrie absolue.



Tag

0x0303

Type

BYTE

Count

1

0-perception 1-Colorimétrie relative 2-saturation 3-Colorimétrie absolue



 

## <a name="propertytagimagetitle"></a>PropertyTagImageTitle

Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x0320                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagresolutionxunit"></a>PropertyTagResolutionXUnit

Unités dans lesquelles afficher la résolution horizontale.



Tag

0x5001

Type

PropertyTagTypeShort

Count

1

1-pixels par pouce 2-pixels par centimètre



 

## <a name="propertytagresolutionyunit"></a>PropertyTagResolutionYUnit

Unités dans lesquelles afficher la résolution verticale.



Tag

0x5002

Type

PropertyTagTypeShort

Count

1

1-pixels par pouce 2-pixels par centimètre



 

## <a name="propertytagresolutionxlengthunit"></a>PropertyTagResolutionXLengthUnit

Unités dans lesquelles afficher la largeur de l’image.



Tag

0x5003

Type

PropertyTagTypeShort

Count

1

1-pouces 2-centimètres 3-points 4-picas 5-colonnes



 

## <a name="propertytagresolutionylengthunit"></a>PropertyTagResolutionYLengthUnit

Unités dans lesquelles afficher la hauteur de l’image.



Tag

0x5004

Type

PropertyTagTypeShort

Count

1

1-pouces 2-centimètres 3-points 4-picas 5-colonnes



 

## <a name="propertytagprintflags"></a>PropertyTagPrintFlags

Séquence de valeurs booléennes sur un octet qui spécifient des options d’impression.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5005               |
| Type  | PropertyTagTypeASCII |
| Nombre | Nombre d’indicateurs      |



 

## <a name="propertytagprintflagsversion"></a>PropertyTagPrintFlagsVersion

Version des indicateurs d’impression.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5006               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagprintflagscrop"></a>PropertyTagPrintFlagsCrop

Afficher le Centre des indicateurs de rognages.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5007              |
| Type  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>PropertyTagPrintFlagsBleedWidth

Largeur du fonds perdus des indicateurs d’impression.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5008              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>PropertyTagPrintFlagsBleedWidthScale

Échelle de la largeur du fonds perdus des indicateurs d’impression.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5009               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaghalftonelpi"></a>PropertyTagHalftoneLPI

Fréquence d’écran de l’encre, en lignes par pouce.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x500A                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>PropertyTagHalftoneLPIUnit

Unités pour la fréquence d’écran.



Tag

0x500B

Type

PropertyTagTypeShort

Count

1

1-lignes par pouce 2 lignes par centimètre



 

## <a name="propertytaghalftonedegree"></a>PropertyTagHalftoneDegree

Angle pour l’écran.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x500C                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftoneshape"></a>PropertyTagHalftoneShape

Forme des points en demi-teinte.



Tag

0x500D

Type

PropertyTagTypeShort

Count

1

0-rond 1-ellipse 2-ligne 3-carré 4-Croix 6-losange



 

## <a name="propertytaghalftonemisc"></a>PropertyTagHalftoneMisc

Informations diverses sur les demi-teintes.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x500E              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytaghalftonescreen"></a>PropertyTagHalftoneScreen

Valeur booléenne qui spécifie s’il faut utiliser les écrans par défaut de l’imprimante.



Tag

0x500F

Type

PropertyTagTypeByte

Count

1

1-utiliser les écrans par défaut de l’imprimante 2-autres



 

## <a name="propertytagjpegquality"></a>PropertyTagJPEGQuality

Balise privée utilisée par le format Adobe Photoshop. Pas d’usage public.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5010               |
| Type  | PropertyTagTypeShort |
| Nombre | Quelconque                  |



 

## <a name="propertytaggridsize"></a>PropertyTagGridSize

Bloc d’informations sur les grilles et les repères.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x5011                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="propertytagthumbnailformat"></a>PropertyTagThumbnailFormat

Format de l’image miniature.



Tag

0x5012

Type

PropertyTagTypeLong

Count

1

0-RAW RGB 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>PropertyTagThumbnailWidth

Largeur, en pixels, de l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5013              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailheight"></a>PropertyTagThumbnailHeight

Hauteur, en pixels, de l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5014              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>PropertyTagThumbnailColorDepth

bits par pixel (BPP) pour l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5015               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>PropertyTagThumbnailPlanes

Nombre de plans de couleur pour l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5016               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>PropertyTagThumbnailRawBytes

Décalage d’octet entre les lignes de données de pixels.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5017              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailsize"></a>PropertyTagThumbnailSize

Taille totale, en octets, de l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5018              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>PropertyTagThumbnailCompressedSize

Taille compressée, en octets, de l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5019              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>PropertyTagColorTransferFunction

Table de valeurs qui spécifient des fonctions de transfert de couleurs.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x501A                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="propertytagthumbnaildata"></a>PropertyTagThumbnailData

Bits de miniature brut au format JPEG ou RGB. Dépend de PropertyTagThumbnailFormat.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x501B              |
| Type  | PropertyTagTypeByte |
| Nombre | Variable            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

Nombre de pixels par ligne dans l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x5020                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>PropertyTagThumbnailImageHeight

Nombre de lignes de pixels dans l’image miniature.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x5021                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>PropertyTagThumbnailBitsPerSample

Nombre de bits par composant de couleur dans l’image miniature. Voir aussi [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).



| Informations sur la propriété | Value |
|-------|-----------------------------------------------------------------|
| Tag   | 0x5022                                                          |
| Type  | PropertyTagTypeShort                                            |
| Nombre | Nombre d’échantillons (composants) par pixel dans l’image miniature |



 

## <a name="propertytagthumbnailcompression"></a>PropertyTagThumbnailCompression

Schéma de compression utilisé pour les données de l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5023               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>PropertyTagThumbnailPhotometricInterp

Interprétation des données de pixels miniatures.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5024               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>PropertyTagThumbnailImageDescription

Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x5025                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagthumbnailequipmake"></a>PropertyTagThumbnailEquipMake

Chaîne de caractères se terminant par un caractère null qui spécifie le fabricant de l’équipement utilisé pour enregistrer l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x5026                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagthumbnailequipmodel"></a>PropertyTagThumbnailEquipModel

Chaîne de caractères se terminant par un caractère null qui spécifie le nom du modèle ou le numéro de modèle de l’équipement utilisé pour enregistrer l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x5027                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagthumbnailstripoffsets"></a>PropertyTagThumbnailStripOffsets

Pour chaque bande dans l’image miniature, le décalage d’octet de cette bande. Voir aussi [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) et [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x5028                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Nombre | Nombre de bandes                            |



 

## <a name="propertytagthumbnailorientation"></a>PropertyTagThumbnailOrientation

Orientation de l’image miniature en termes de lignes et de colonnes. Voir aussi [PropertyTagOrientation](#propertytagorientation).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5029               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>PropertyTagThumbnailSamplesPerPixel

Nombre de composants de couleur par pixel dans l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x502A               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>PropertyTagThumbnailRowsPerStrip

Nombre de lignes par bande dans l’image miniature. Voir aussi [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) et [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x502B                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>PropertyTagThumbnailStripBytesCount

Pour chaque bande d’images miniatures, nombre total d’octets dans cette bande.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0x502C                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Nombre | Nombre de bandes dans l’image miniature     |



 

## <a name="propertytagthumbnailresolutionx"></a>PropertyTagThumbnailResolutionX

Résolution des miniatures dans le sens de la largeur. L’unité de résolution est donnée dans [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informations sur la propriété | Value |
|-----|--------|
| Tag | 0x502D |



 

## <a name="propertytagthumbnailresolutiony"></a>PropertyTagThumbnailResolutionY

Résolution des miniatures dans le sens de la hauteur. L’unité de résolution est donnée dans [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informations sur la propriété | Value |
|-----|--------|
| Tag | 0x502E |



 

## <a name="propertytagthumbnailplanarconfig"></a>PropertyTagThumbnailPlanarConfig

Si les composants de pixels de l’image miniature sont enregistrés au format de forme groupée ou planaire. Voir aussi [PropertyTagPlanarConfig](#propertytagplanarconfig).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x502F               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>PropertyTagThumbnailResolutionUnit

Unité de mesure pour la résolution horizontale et la résolution verticale de l’image miniature. Voir aussi [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5030               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>PropertyTagThumbnailTransferFunction

Tables qui spécifient des fonctions de transfert pour l’image miniature. Voir aussi [PropertyTagTransferFunction](#propertytagtransferfunction).



| Informations sur la propriété | Value |
|-------|------------------------------------------------------|
| Tag   | 0x5031                                               |
| Type  | PropertyTagTypeShort                                 |
| Nombre | Nombre total de mots de 16 bits requis pour les tables |



 

## <a name="propertytagthumbnailsoftwareused"></a>PropertyTagThumbnailSoftwareUsed

Chaîne de caractères se terminant par un caractère null qui spécifie le nom et la version du logiciel ou du microprogramme de l’appareil utilisé pour générer l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x5032                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagthumbnaildatetime"></a>PropertyTagThumbnailDateTime

Date et heure de création de l’image miniature. Voir aussi [PropertyTagDateTime](#propertytagdatetime).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5033               |
| Type  | PropertyTagTypeASCII |
| Nombre | 20                   |



 

## <a name="propertytagthumbnailartist"></a>PropertyTagThumbnailArtist

Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la personne qui a créé l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x5034                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagthumbnailwhitepoint"></a>PropertyTagThumbnailWhitePoint

Chromatique du point blanc de l’image miniature. Voir aussi [PropertyTagWhitePoint](#propertytagwhitepoint).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x5035                  |
| Type  | PropertyTagTypeRational |
| Nombre | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>PropertyTagThumbnailPrimaryChromaticities

Pour chacune des trois couleurs primaires dans l’image miniature, la chromatique de cette couleur. Voir aussi [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x5036                  |
| Type  | PropertyTagTypeRational |
| Nombre | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>PropertyTagThumbnailYCbCrCoefficients

Coefficients pour la transformation des données RVB en données YCbCr pour l’image miniature. Voir aussi [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x5037                  |
| Type  | PropertyTagTypeRational |
| Nombre | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>PropertyTagThumbnailYCbCrSubsampling

Taux d’échantillonnage des composants de chrominance par rapport au composant luminance pour l’image miniature. Voir aussi [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5038               |
| Type  | PropertyTagTypeShort |
| Nombre | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>PropertyTagThumbnailYCbCrPositioning

Position des composants de chrominance par rapport au composant luminance pour l’image miniature. Voir aussi [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5039               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>PropertyTagThumbnailRefBlackWhite

Valeur du point noir de référence et valeur du point blanc de référence pour l’image miniature. Voir aussi [PropertyTagREFBlackWhite](#propertytagrefblackwhite).



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x503A                  |
| Type  | PropertyTagTypeRational |
| Nombre | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>PropertyTagThumbnailCopyRight

Chaîne de caractères se terminant par un caractère null qui contient les informations de copyright pour l’image miniature.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x503B                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagluminancetable"></a>PropertyTagLuminanceTable

Table de luminance. La table de luminance et la table de chrominance sont utilisées pour contrôler la qualité JPEG. Une table de luminance ou de chrominance valide a 64 entrées de type PropertyTagTypeShort. Si une image a une table de luminance ou une table de chrominance, elle doit avoir les deux tables.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5090               |
| Type  | PropertyTagTypeShort |
| Nombre | 64                   |



 

## <a name="propertytagchrominancetable"></a>PropertyTagChrominanceTable

Table de chrominance. La table de luminance et la table de chrominance sont utilisées pour contrôler la qualité JPEG. Une table de luminance ou de chrominance valide a 64 entrées de type PropertyTagTypeShort. Si une image a une table de luminance ou une table de chrominance, elle doit avoir les deux tables.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5091               |
| Type  | PropertyTagTypeShort |
| Nombre | 64                   |



 

## <a name="propertytagframedelay"></a>PropertyTagFrameDelay

Délai, en centièmes de seconde, entre deux frames dans une image GIF animée.



| Informations sur la propriété | Value |
|-------|-------------------------------|
| Tag   | 0x5100                        |
| Type  | PropertyTagTypeLong           |
| Nombre | Nombre de frames dans l’image |



 

## <a name="propertytagloopcount"></a>PropertyTagLoopCount

Pour une image GIF animée, le nombre d’affichages de l’animation. La valeur 0 spécifie que l’animation doit être affichée de façon infinie.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x5101               |
| Type  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagglobalpalette"></a>PropertyTagGlobalPalette

Palette de couleurs pour une bitmap indexée dans une image GIF.



| Informations sur la propriété | Value |
|-------|-------------------------------|
| Tag   | 0x5102                        |
| Type  | PropertyTagTypeByte           |
| Nombre | 3 x nombre d’entrées de palette |



 

## <a name="propertytagindexbackground"></a>PropertyTagIndexBackground

Index de la couleur d’arrière-plan dans la palette d’une image GIF.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5103              |
| Type  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagindextransparent"></a>PropertyTagIndexTransparent

Index de la couleur transparente dans la palette d’une image GIF.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5104              |
| Type  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagpixelunit"></a>PropertyTagPixelUnit

Unité pour PropertyTagPixelPerUnitX et PropertyTagPixelPerUnitY.



Tag

0x5110

Type

PropertyTagTypeByte

Count

1

0-Inconnu



 

## <a name="propertytagpixelperunitx"></a>PropertyTagPixelPerUnitX

Pixels par unité sur l’axe x.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5111              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpixelperunity"></a>PropertyTagPixelPerUnitY

Pixels par unité dans l’axe y.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x5112              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpalettehistogram"></a>PropertyTagPaletteHistogram

Histogramme de la palette.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x5113                  |
| Type  | PropertyTagTypeByte     |
| Nombre | Longueur de l’histogramme |



 

## <a name="propertytagcopyright"></a>PropertyTagCopyright

Chaîne de caractères se terminant par un caractère null qui contient des informations de copyright.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x8298                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagexifexposuretime"></a>PropertyTagExifExposureTime

Temps d’exposition, mesuré en secondes.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x829A                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffnumber"></a>PropertyTagExifFNumber

Numéro F.



| Informations sur la propriété | Value |
|-------|----------|
| Tag   | 0x829D   |
| Type  | RATIONNELLE |
| Count | 1        |



 

## <a name="propertytagexififd"></a>PropertyTagExifIFD

Balise privée utilisée par GDI+. Pas d’usage public. GDI+ utilise cette balise pour localiser des informations spécifiques à EXIF.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x8769              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagiccprofile"></a>PropertyTagICCProfile

Profil ICC incorporé dans l’image.



| Informations sur la propriété | Value |
|-------|-----------------------|
| Tag   | 0x8773                |
| Type  | PropertyTagTypeByte   |
| Nombre | Longueur du profil |



 

## <a name="propertytagexifexposureprog"></a>PropertyTagExifExposureProg

Classe du programme utilisée par l’appareil photo pour définir l’exposition lorsque l’image est prise.



Tag

0x8822

Type

SHORT

Count

1

Default

0

0-non défini 1-Manuel 2-programme normal 3-priorité 4-priorité 5-programme créatif (en faveur de la profondeur du champ) 6-Programme d’action (biaisé vers rapide) Vitesse d’obturation) 7-mode Portrait (pour les photos de plus haut en arrière-plan) 8-mode paysage (pour les photos en mode paysage avec l’arrière-plan) 9 à 255-réservé



 

## <a name="propertytagexifspectralsense"></a>PropertyTagExifSpectralSense

Chaîne de caractères se terminant par un caractère null qui spécifie la sensibilité spectrale de chaque canal de l’appareil photo utilisé. La chaîne est compatible avec la norme développée par le Comité technique ASTM.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x8824                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytaggpsifd"></a>PropertyTagGpsIFD

Décalage d’un bloc d’éléments de propriété GPS. Les éléments de propriété dont les balises ont le préfixe PropertyTagGps sont stockés dans le bloc GPS. Les éléments de propriété GPS sont définis dans la spécification EXIF. GDI+ utilise cette balise pour localiser les informations GPS, mais GDI+ n’expose pas cette balise pour une utilisation publique.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0x8825              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifisospeed"></a>PropertyTagExifISOSpeed

Vitesse ISO et ISO latitude de l’appareil photo ou de l’appareil d’entrée comme spécifié dans la norme ISO 12232.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x8827               |
| Type  | PropertyTagTypeShort |
| Nombre | Quelconque                  |



 

## <a name="propertytagexifoecf"></a>PropertyTagExifOECF

Fonction de conversion optoélectronique (OECF) spécifiée dans ISO 14524. Le OECF est la relation entre l’entrée optique de l’appareil photo et les valeurs de l’image.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x8828                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="propertytagexifver"></a>PropertyTagExifVer

Version de la norme EXIF prise en charge. L’absence de ce champ est utilisée pour signifier la non-conformité à la norme. La conformité à la norme est indiquée par l’enregistrement de 0210 sous la forme d’une chaîne ASCII sur 4 octets. Étant donné que le type est PropertyTagTypeUndefined, il n’y a aucune marque de fin NULL.



| Informations sur la propriété | Value |
|---------|--------------------------|
| Tag     | 0x9000                   |
| Type    | PropertyTagTypeUndefined |
| Nombre   | 4                        |
| Default | 0210                     |



 

## <a name="propertytagexifdtorig"></a>PropertyTagExifDTOrig

Date et heure de génération des données de l’image d’origine. Pour un DSC, date et heure auxquelles l’image a été prise. Le format est YYYY : MM : JJ HH : MM : SS avec l’heure affichée au format 24 heures et la date et l’heure séparées par un caractère vide (0x2000). La longueur de la chaîne de caractères est de 20 octets, y compris le terminateur NULL. Lorsque le champ est vide, il est considéré comme inconnu.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x9003               |
| Type  | PropertyTagTypeASCII |
| Nombre | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>PropertyTagExifDTDigitized

Date et heure auxquelles l’image a été stockée en tant que données numériques. Si, par exemple, une image a été capturée par DSC et qu’au même moment, le fichier a été enregistré, DateTimeOriginal et DateTimeDigitized auront le même contenu.

Le format est YYYY : MM : JJ HH : MM : SS avec l’heure affichée au format 24 heures et la date et l’heure séparées par un caractère vide (0x2000). La longueur de la chaîne de caractères est de 20 octets, y compris le terminateur NULL. Lorsque le champ est vide, il est considéré comme inconnu.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0x9004               |
| Type  | PropertyTagTypeASCII |
| Nombre | 20                   |



 

## <a name="propertytagexifcompconfig"></a>PropertyTagExifCompConfig

Informations spécifiques aux données compressées. Les canaux de chaque composant sont organisés dans l’ordre du premier composant au quatrième. Pour les données non compressées, la disposition des données est indiquée dans la balise PropertyTagPhotometricInterp.

Toutefois, étant donné que PropertyTagPhotometricInterp peut uniquement exprimer l’ordre de Y, CB et CR, cette balise est fournie pour les cas où les données compressées utilisent des composants autres que Y, CB et CR et pour prendre en charge d’autres séquences.



Tag

0x9101

Type

PropertyTagTypeUndefined

Nombre

4

Default

4 5 6 0 (si RVB non compressé) 1 2 3 0 (autres cas)

0-n’existe pas 1-Y 2-CB 3-CR 4-R 5-G 6-B autre-réservé



 

## <a name="propertytagexifcompbpp"></a>PropertyTagExifCompBPP

Informations spécifiques aux données compressées. Le mode de compression utilisé pour une image compressée est indiqué dans unités BPP.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x9102                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>PropertyTagExifShutterSpeed

Vitesse d’obturation. L’unité est la valeur système additive de l’exposition photographique (APEX).



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x9201                   |
| Type  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifaperture"></a>PropertyTagExifAperture

Ouverture de l’objectif. L’unité est la valeur APEX.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x9202                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifbrightness"></a>PropertyTagExifBrightness

Valeur de luminosité. L’unité est la valeur APEX. En règle générale, elle est indiquée dans la plage de-99,99 à 99,99.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x9203                   |
| Type  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifexposurebias"></a>PropertyTagExifExposureBias

Décalage de l’exposition. L’unité est la valeur APEX. En règle générale, elle est comprise entre-99,99 et 99,99.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x9204                   |
| Type  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>PropertyTagExifMaxAperture

Plus petit numéro F de la lentille. L’unité est la valeur APEX. En règle générale, elle est comprise dans la plage de 00,00 à 99,99, mais elle n’est pas limitée à cette plage.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x9205                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>PropertyTagExifSubjectDist

Distance à l’objet, mesurée en mètres.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x9206                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>PropertyTagExifMeteringMode

Mode de contrôle.



Tag

0x9207

Type

PropertyTagTypeShort

Count

1

Default

0

0-Unknown 1-Average 2-CenterWeightedAverage 3-Spot 4-multipoint 5-pattern 6-partial 7 à 254-reserved 255-Other



 

## <a name="propertytagexiflightsource"></a>PropertyTagExifLightSource

Type de source de lumière.



Tag

0x9208

Type

PropertyTagTypeShort

Count

1

Default

0

0-Inconnu 1-heure d’été 2-fluorescents 3-tungstène 17-standard lumière 18-standard clair B 19-standard Light C 20-D55 21-D65 22-D75 23 254-réservé 255-Other



 

## <a name="propertytagexifflash"></a>PropertyTagExifFlash

État Flash. Cette balise est enregistrée lorsqu’une image est prise à l’aide d’une lumière stroboscopique (Flash). Le bit 0 indique l’état de déclenchement Flash et les bits 1 et 2 indiquent l’état de retour du flash.



Tag

0x9209

Type

PropertyTagTypeShort

Count

1

Valeurs de bit 0 qui indiquent si le flash s’est déclenché : 0b-Flash n’a pas déclenché 1b-Flash déclenché

Valeurs pour bits 1 et 2 qui indiquent l’état de la lumière renvoyée : 00B-aucune fonction de détection de retour de lumière 01b-réservée 10 b-lumière de retour stroboscopique non détectée 11B-lumière de retour stroboscopique détectée

Valeurs de balise Flash résultantes : 0x0000-Flash n’a pas déclenché 0x0001-Flash déclenché 0x0005-lumière de retour stroboscopique non détectée



 

## <a name="propertytagexiffocallength"></a>PropertyTagExifFocalLength

Longueur focale réelle, en millimètres, de la lentille. La conversion n’est pas effectuée à la longueur focale d’une caméra de film 35 millimètres.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0x920A                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmakernote"></a>PropertyTagExifMakerNote

Étiquette de note. Balise utilisée par les fabricants de rédacteurs EXIF pour enregistrer des informations. Le contenu est destiné au fabricant.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x927C                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="propertytagexifusercomment"></a>PropertyTagExifUserComment

Balise de commentaire. Balise utilisée par les utilisateurs EXIF pour écrire des mots clés ou des commentaires sur l’image en plus de ceux de PropertyTagImageDescription et sans les limitations de code de caractères de la balise PropertyTagImageDescription.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0x9286                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

Le code de caractère utilisé dans la balise PropertyTagExifUserComment est identifié en fonction d’un code d’ID dans une zone fixe de 8 octets au début de la zone de données de la balise. La partie inutilisée de la zone est remplie avec des caractères null (0). Les codes d’ID sont affectés par le biais de l’inscription. Étant donné que le type n’est pas ASCII, il n’est pas nécessaire d’utiliser une marque de fin NULL.

## <a name="propertytagexifdtsubsec"></a>PropertyTagExifDTSubsec

Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagDateTime.



| Informations sur la propriété | Value |
|-------|----------------------------------------------------|
| Tag   | 0x9290                                             |
| Type  | PropertyTagTypeASCII                               |
| Nombre | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagexifdtorigss"></a>PropertyTagExifDTOrigSS

Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagExifDTOrig.



| Informations sur la propriété | Value |
|------|----------------------------------------------------|
| Tag  | 0x9291                                             |
| Type | PropertyTagTypeASCII                               |
| N    | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagexifdtdigss"></a>PropertyTagExifDTDigSS

Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagExifDTDigitized.



| Informations sur la propriété | Value |
|------|----------------------------------------------------|
| Tag  | 0x9292                                             |
| Type | ASCII                                              |
| N    | Longueur de la chaîne, y compris la marque de fin NULL |



 

## <a name="propertytagexiffpxver"></a>PropertyTagExifFPXVer

Version du format FlashPix prise en charge par un fichier FPXR. Si la fonction FPXR prend en charge le format FlashPix version 1,0, cela est indiqué de la même façon que PropertyTagExifVer en enregistrant 0100 comme chaîne ASCII de 4 octets. Étant donné que le type est PropertyTagTypeUndefined, il n’y a aucune marque de fin NULL.



Tag

0xA000

Type

PropertyTagTypeUndefined

Nombre

4

Default

0100

0100-version du format FlashPix 1,0 autre-réservé



 

## <a name="propertytagexifcolorspace"></a>PropertyTagExifColorSpace

Spécificateur d’espace colorimétrique. Normalement, sRVB (= 1) est utilisé pour définir l’espace colorimétrique en fonction des conditions et de l’environnement du moniteur PC. Si un espace de couleurs autre que sRVB est utilisé, non étalonné (= 0xFFFF) est défini. Les données d’image enregistrées comme non calibrées peuvent être traitées comme sRVB lorsqu’elles sont converties en FlashPix.



Tag

0xA001

Type

PropertyTagTypeShort

Count

1

0x1-sRVB 0xFFFF-non étalonné autre-réservé



 

## <a name="propertytagexifpixxdim"></a>PropertyTagExifPixXDim

Informations spécifiques aux données compressées. Lorsqu’un fichier compressé est enregistré, la largeur valide de l’image explicite doit être enregistrée dans cette balise, qu’il y ait ou non des données de remplissage ou un marqueur de redémarrage. Cette balise ne doit pas exister dans un fichier non compressé.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0xA002                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifpixydim"></a>PropertyTagExifPixYDim

Informations spécifiques aux données compressées. Lorsqu’un fichier compressé est enregistré, la hauteur valide de l’image explicite doit être enregistrée dans cette balise, qu’il y ait ou non des données de remplissage ou un marqueur de redémarrage. Cette balise ne doit pas exister dans un fichier non compressé. Étant donné que le remplissage des données n’est pas nécessaire dans le sens vertical, le nombre de lignes enregistrées dans cette balise de hauteur d’image valide sera le même que celui enregistré dans le SOF.



| Informations sur la propriété | Value |
|-------|---------------------------------------------|
| Tag   | 0xA003                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>PropertyTagExifRelatedWav

Nom d’un fichier audio associé aux données de l’image. Les seules informations relationnelles enregistrées sont le nom et l’extension du fichier audio EXIF (une chaîne ASCII composée de 8 caractères plus un point (.), plus 3 caractères). Le chemin d’accès n’est pas enregistré. Lorsque vous utilisez cette balise, les fichiers audio doivent être enregistrés conformément au format audio EXIF. Les enregistreurs peuvent également stocker des données audio dans APP2 sous forme de données de flux d’extension FlashPix.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0xA004               |
| Type  | PropertyTagTypeASCII |
| Nombre | 13                   |



 

## <a name="propertytagexifinterop"></a>PropertyTagExifInterop

Décalage d’un bloc d’éléments de propriété qui contiennent des informations d’interopérabilité.



| Informations sur la propriété | Value |
|-------|---------------------|
| Tag   | 0xA005              |
| Type  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifflashenergy"></a>PropertyTagExifFlashEnergy

Énergie stroboscopique, en secondes de puissance de la bougie (BCPS), au moment où l’image a été capturée.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0xA20B                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifspatialfr"></a>PropertyTagExifSpatialFR

Table de fréquence spatiale des appareils d’entrée et de caméra et valeurs SFR dans la largeur de l’image, la hauteur de l’image et la direction diagonale, comme spécifié dans la norme ISO 12233.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0xA20C                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="propertytagexiffocalxres"></a>PropertyTagExifFocalXRes

Nombre de pixels dans la direction de l’image (x) par unité sur le plan focal de l’appareil photo. L’unité est spécifiée dans PropertyTagExifFocalResUnit.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0xA20E                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalyres"></a>PropertyTagExifFocalYRes

Nombre de pixels dans la direction de la hauteur d’image (y) par unité sur le plan focal de l’appareil photo. L’unité est spécifiée dans PropertyTagExifFocalResUnit.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0xA20F                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>PropertyTagExifFocalResUnit

Unité de mesure pour PropertyTagExifFocalXRes et PropertyTagExifFocalYRes.



Tag

0xA210

Type

PropertyTagTypeShort

Count

1

2 pouces, 3-centimètres



 

## <a name="propertytagexifsubjectloc"></a>PropertyTagExifSubjectLoc

Emplacement du sujet principal de la scène. La valeur de cette balise représente le pixel au centre du sujet principal par rapport au bord gauche. La première valeur indique le numéro de colonne, tandis que la deuxième valeur indique le numéro de ligne.



| Informations sur la propriété | Value |
|-------|----------------------|
| Tag   | 0xA214               |
| Type  | PropertyTagTypeShort |
| Nombre | 2                    |



 

## <a name="propertytagexifexposureindex"></a>PropertyTagExifExposureIndex

Index d’exposition sélectionné sur l’appareil photo ou l’appareil d’entrée au moment où l’image a été capturée.



| Informations sur la propriété | Value |
|-------|-------------------------|
| Tag   | 0xA215                  |
| Type  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>PropertyTagExifSensingMethod

Type de capteur d’image sur l’appareil photo ou le périphérique d’entrée.



Tag

0xA217

Type

PropertyTagTypeShort

Count

1

capteur de zone de couleur à deux puces non défini (2-un), capteur de zone de couleur à deux processeurs 4-capteur de zone de couleur à trois puces-capteur de zone de couleur séquentielle 7-capteur trilinéaire 8-capteur linéaire séquentiel en couleur



 

## <a name="propertytagexiffilesource"></a>PropertyTagExifFileSource

Source de l’image. Si un DSC a enregistré l’image, la valeur de cette balise est 3.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0xA300                   |
| Type  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifscenetype"></a>PropertyTagExifSceneType

Type de scène. Si un DSC a enregistré l’image, la valeur de cette balise doit être définie sur 1, ce qui indique que l’image a été directement photographiée.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0xA301                   |
| Type  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifcfapattern"></a>PropertyTagExifCfaPattern

Motif géométrique CFA (Color Filter Array) du capteur d’images lorsqu’un capteur de zone de couleurs à une seule puce est utilisé. Elle ne s’applique pas à toutes les méthodes de détection.



| Informations sur la propriété | Value |
|-------|--------------------------|
| Tag   | 0xA302                   |
| Type  | PropertyTagTypeUndefined |
| Nombre | Quelconque                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécifications des formats de fichiers image](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Constantes de balise de propriété d’image](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**Constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[Balises de propriété par ordre alphabétique](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[Balises de propriété dans l’ordre numérique](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[Lecture et écriture de métadonnées](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



