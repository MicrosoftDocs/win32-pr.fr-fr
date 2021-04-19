---
description: Le décodeur MP3 Windows Media décode les fichiers audio qui ont été encodés dans les formats suivants.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Décodeur MP3 Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542736"
---
# <a name="windows-media-mp3-decoder"></a>Décodeur MP3 Windows Media

Le décodeur MP3 Windows Media décode les fichiers audio qui ont été encodés dans les formats suivants.

-   ISO/IEC 11172-3 (MPEG-1 audio) couche 3
-   ISO/IEC 13818-3 (MPEG-2 audio) couche 3, extension de fréquence d’échantillonnage faible

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur MP3 Windows Media est représenté par la constante **CLSID \_ CMP3DecMediaObject**. Vous pouvez créer une instance du décodeur MP3 en appelant **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objet décodeur MP3 expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un décodeur MP3 Windows Media se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant indique les conditions sous lesquelles un décodeur MP3 Windows Media se comporte comme un DMO ou une table MFT.



| Système d’exploitation | Comportement du décodeur                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un décodeur MP3 Windows Media se comporte toujours comme un DMO.                                                                                                                                           |
| Windows Vista    | Par défaut, un décodeur MP3 Windows Media se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un décodeur MP3 Windows Media, il se comporte comme une table MFT. |
| Windows 7        | Par défaut, un décodeur MP3 Windows Media se comporte comme un DMO. Si vous obtenez une interface **IMFTransform** sur un décodeur MP3 Windows Media, il se comporte comme une table MFT.                                    |



 

## <a name="input-formats"></a>Formats d’entrée

Le tableau suivant montre la balise de format audio qui représente le type d’entrée pris en charge par le décodeur MP3 Windows Media.



| Balise de format, constante      | Mettre en forme la valeur de balise | Format audio     |
|--------------------------|------------------|------------------|
| \_MPEGLAYER3 format \_ Wave | 0x55             | Couche MPEG ISO 3 |



 

## <a name="output-formats"></a>Formats de sortie

Le tableau suivant répertorie les balises de format audio qui représentent les types de sortie pris en charge par le décodeur MP3 Windows Media.



| Balise de format, constante       | Mettre en forme la valeur de balise | Format audio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| \_PCM format \_ Wave         | 0x0001           | Format PCM (en cas d’utilisation comme DMO ou MFT)                                   |
| \_format Wave \_ IEEE \_ float | 0x0003           | Virgule flottante IEEE (en cas d’utilisation en tant que MFT)                                   |
| \_format Wave \_ extensible  | 0xFFFE           | Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE** (en cas d’utilisation en tant que MFT) |



 

Le décodeur MP3 Windows Media prend en charge et énumère les types de médias de sortie suivants.

-   Type de sortie qui a le même taux d’échantillonnage et le même nombre de canaux que le type d’entrée.
-   Sortie mono pour une entrée stéréo.
-   Types de sortie avec des profondeur de bit de 8 et 16.
-   Sortie à virgule flottante, si le décodeur se comporte comme une table MFT.

Le décodeur MP3 Windows Media prend en charge, mais n’énumère pas les types de médias de sortie suivants.

-   Type de sortie qui a la moitié du taux d’échantillonnage du type d’entrée.
-   Type de sortie qui a un quatrième taux d’échantillonnage du type d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> </dl>

 

 




