---
description: Cette vue d’ensemble décrit le format RIFF (Resource Interchange File Format), qui est utilisé dans les fichiers. wav. RIFF est le format standard à partir duquel les données audio pour XAudio2 sont chargées.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535046"
---
# <a name="resource-interchange-file-format-riff"></a>RIFF (Resource Interchange File Format)

Cette vue d’ensemble décrit le format RIFF (Resource Interchange File Format), qui est utilisé dans les fichiers. wav. RIFF est le format standard à partir duquel les données audio pour XAudio2 sont chargées.

## <a name="riff"></a>RIFF

Un fichier RIFF est constitué de plusieurs sections discrètes de données appelées *segments*.

## <a name="fourcc-identifiers"></a>Identificateurs FOURCC

Le type de données d’un segment est indiqué par un identificateur de code à quatre caractères (FOURCC). Un FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII utilisés pour identifier les types de blocs dans un fichier RIFF. Par exemple, le FOURCC « ABCD » est représenté sur un système Little endian en tant que 0x64636261. FOURCCs peut contenir des espaces, « ABC » est donc un FOURCC valide. Les fichiers audio utilisent des Codes FOURCC pour identifier les blocs de format audio, les segments de données audio et tout autre segment spécifique au format audio.

Le tableau suivant présente les identificateurs FOURCC qui peuvent être attendus dans les formats audio pris en charge par XAudio2. 

| Format | Identificateurs FOURCC                     | Informations supplémentaires                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | « RIFF », « fmt », « données »                 |                                                                                                      |
| ADPCM  | « RIFF », « fmt », « Data », « SMPL », « wsmpl » | Pour obtenir une description des identificateurs FOURCC spécifiques à ADPCM, voir [vue d’ensemble d’ADPCM](adpcm-overview.md) . |



 

Les identificateurs FOURCC « RIFF », « fmt » et « Data » sont communs à tous les formats pris en charge. Le tableau suivant décrit les identificateurs FOURCC qui se trouvent dans tous les formats pris en charge. 

| Identificateur FOURCC | Description                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | Bloc RIFF standard contenant un type de fichier avec la valeur « WAVE » ou « XWMA » dans les quatre premiers octets de sa section de données et les autres segments du fichier dans le reste de sa section de données.                                   |
| "fmt"             | Contient l’en-tête de format du fichier audio. Les données de ce segment correspondent à l’une des structures suivantes : **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| "data"            | Contient des données audio pour le fichier audio. Dans XAudio2, le contenu du segment de données est lu dans une mémoire tampon et transmis à une voix source en tant que membre **pAudioData** d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . |



 

## <a name="chunks"></a>Chunks

Un fichier RIFF se compose d’un bloc RIFF contenant zéro ou plusieurs autres segments.

-   Le bloc RIFF se présente sous la forme suivante :

    « RIFF », fileSize, fileType, données

    Où « RIFF » est le littéral de code FOURCC « RIFF », *FileSize* est une valeur de 4 octets qui donne la taille des données dans le fichier et *FILETYPE* est un FourCC qui identifie le type de fichier spécifique. La valeur de *FileSize* inclut la taille du FourCC de *filetype* plus la taille des données qui suivent, mais n’inclut pas la taille du FourCC « riff » ou la taille du *FileSize*. Les données se composent de segments dans n’importe quel ordre.

-   Les autres blocs se présentent sous la forme suivante :

    ```
    chunkID, chunkSize, data
    ```

    

    Où *chunkID* est un FourCC qui identifie les données contenues dans le bloc, *chunkSize* est une valeur de 4 octets qui donne la taille de la section de données du segment, et les données contiennent zéro, un ou plusieurs octets de données. Les données sont toujours complétées à la limite de mot la plus proche. *chunkSize* indique la taille des données valides dans le bloc. Elle n’inclut pas le remplissage, la taille de *chunkID* ou la taille de *chunkSize*.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Procédure : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Référence de programmation XAudio2](programming-reference.md)
</dt> </dl>

 

 



