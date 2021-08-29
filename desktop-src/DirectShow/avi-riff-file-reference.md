---
description: Référence de fichier RIFF AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Référence de fichier RIFF AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68cfe9cd0ef27f5aa7a02870392938e14f84caa1a041b0f7677ddbd703920bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794589"
---
# <a name="avi-riff-file-reference"></a>Référence de fichier RIFF AVI

Le format de fichier Microsoft AVI est une spécification de fichier RIFF utilisée avec les applications qui capturent, modifient et lisent des séquences audio-video. En général, les fichiers AVI contiennent plusieurs flux de différents types de données. La plupart des séquences AVI utilisent à la fois des flux audio et vidéo. Une variation simple pour une séquence AVI utilise des données vidéo et ne nécessite pas de flux audio.

Cette section ne décrit pas les extensions de format de fichier AVI OpenDML. Pour plus d’informations sur ces extensions, consultez *extensions de format de fichier AVI OpenDML*, publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML.

## <a name="fourccs"></a>FOURCCs

Un code FOURCC (code à quatre caractères) est un entier non signé 32 bits créé par concaténation de quatre caractères ASCII. Par exemple, le FOURCC « ABCD » est représenté sur un système de Little-Endian en tant que 0x64636261. FOURCCs peut contenir des espaces, « ABC » est donc un FOURCC valide. Le format de fichier AVI utilise des Codes FOURCC pour identifier les types de flux, les segments de données, les entrées d’index et d’autres informations.

## <a name="riff-file-format"></a>Format de fichier RIFF

Le format de fichier AVI est basé sur le format de document RIFF (Resource Interchange File Format). Un fichier RIFF se compose d’un en-tête RIFF suivi de zéro, une ou plusieurs *listes* et *segments*.

-   L’en-tête RIFF se présente sous la forme suivante :

    `'RIFF' fileSize fileType (data)`

    où « RIFF » est le littéral de code FOURCC « RIFF », `fileSize` est une valeur de 4 octets qui donne la taille des données dans le fichier et `fileType` est un FourCC qui identifie le type de fichier spécifique. La valeur de `fileSize` inclut la taille du `fileType` FourCC plus la taille des données qui suivent, mais n’inclut pas la taille du FourCC’riff’ou la taille de `fileSize` . Les données de fichier se composent de blocs et de listes, dans n’importe quel ordre.

-   Un segment se présente sous la forme suivante :

    `ckID ckSize ckData`

    où `ckID` est un FourCC qui identifie les données contenues dans le bloc, `ckSize` est une valeur de 4 octets qui donne la taille des données dans `ckData` et `ckData` représente zéro, un ou plusieurs octets de données. Les données sont toujours complétées à la limite de **mot** la plus proche. `ckSize` indique la taille des données valides dans le bloc. elle n’inclut pas le remplissage, la taille `ckID` ou la taille de `ckSize` .

-   Une liste se présente sous la forme suivante :

    `'LIST' listSize listType listData`

    où « LIST » est le littéral de code FOURCC « LIST », `listSize` est une valeur de 4 octets qui donne la taille de la liste, `listType` est un code FourCC et `listData` se compose de segments ou de listes, dans n’importe quel ordre. La valeur de `listSize` inclut la taille de `listType` plus la taille de `listData` ; elle n’inclut pas le FourCC’List’ou la taille de `listSize` .

Le reste de cette section utilise la notation suivante pour décrire les blocs RIFF :

`ckID ( ckData )`

où la taille de segment est implicite. À l’aide de cette notation, une liste peut être représentée comme suit :

`'LIST' ( listType ( listData ) )`

Les éléments facultatifs sont placés entre crochets : `[ optional element ]`

## <a name="avi-riff-form"></a>Forme de formulaire RIFF AVI

Les fichiers AVI sont identifiés par le FOURCC « AVI » dans l’en-tête RIFF. Tous les fichiers AVI incluent deux blocs de liste obligatoires, qui définissent le format des flux et les données de flux, respectivement. Un fichier AVI peut également inclure un segment d’index, qui donne l’emplacement des segments de données dans le fichier. Un fichier AVI avec ces composants se présente sous la forme suivante :


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



La liste « HDRL » définit le format des données et est le premier bloc de liste requis. La liste « movi » contient les données de la séquence AVI et est le deuxième segment de la liste obligatoire. La liste « idx1 » contient l’index. Les fichiers AVI doivent conserver ces trois composants dans l’ordre approprié.

> [!Note]  
> Les extensions OpenDML définissent un autre type d’index, identifié par le FOURCC « indx ».

 

Les listes « HDRL » et « movi » utilisent des sous-segments pour leurs données. L’exemple suivant montre le format AVI d’un AVI développé avec les segments nécessaires pour compléter ces listes :


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>En-tête AVI principal

La liste « HDRL » commence par l’en-tête AVI principal, qui est contenu dans un bloc « AVIH ». L’en-tête principal contient des informations globales sur l’ensemble du fichier AVI, telles que le nombre de flux dans le fichier, ainsi que la largeur et la hauteur de la séquence AVI. Le segment d’en-tête principal se compose d’une structure [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

## <a name="avi-stream-headers"></a>En-têtes de flux AVI

Une ou plusieurs listes « strl » suivent l’en-tête principal. Une liste’strl’est requise pour chaque flux de données. Chaque liste « strl » contient des informations sur un flux du fichier et doit contenir un bloc d’en-tête de flux (« Strh ») et un bloc de format de flux (« Strf »). En outre, une liste « strl » peut contenir un bloc de données d’en-tête de flux (« StrD ») et un segment de nom de flux (« STRN »).

Le bloc d’en-tête de flux ('Strh') se compose d’une structure [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .

Un bloc de format de flux (« Strf ») doit suivre le bloc d’en-tête de flux. Le bloc de format de flux décrit le format des données dans le flux. Les données contenues dans ce segment dépendent du type de flux. Pour les flux vidéo, les informations sont une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , y compris les informations de palette, le cas échéant. Pour les flux audio, les informations sont une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Si le segment de données d’en-tête de flux de données (« StrD ») est présent, il suit le bloc de format de flux. Le format et le contenu de ce segment sont définis par le pilote du codec. En règle générale, les pilotes utilisent ces informations pour la configuration. Les applications qui lisent et écrivent des fichiers AVI n’ont pas besoin d’interpréter ces informations. ils le transfèrent simplement vers et depuis le pilote sous la forme d’un bloc de mémoire.

Le bloc’STRN’facultatif contient une chaîne de texte se terminant par un caractère null qui décrit le flux.

Les en-têtes de flux dans la liste « HDRL » sont associés aux données de flux dans la liste « movi » en fonction de l’ordre des segments « strl ». Le premier segment « strl » s’applique au flux 0, le deuxième s’applique à Stream 1, et ainsi de suite.

## <a name="stream-data-movi-list"></a>Données de flux (liste « movi »)

Le fait de suivre les informations d’en-tête est une liste « movi » qui contient les données réelles dans les flux, c’est-à-dire les images vidéo et les échantillons audio. Les segments de données peuvent résider directement dans la liste « movi », ou ils peuvent être regroupés dans des listes « Rec ». Le regroupement « Rec » implique que les segments groupés doivent être lus à partir du disque en une seule fois et sont destinés aux fichiers qui sont entrelacés pour être lus à partir d’un CD-ROM.

Le FOURCC qui identifie chaque segment de données se compose d’un numéro de flux à deux chiffres suivi d’un code à deux caractères qui définit le type d’informations dans le bloc.



| Code à deux caractères | Description              |
|--------------------|--------------------------|
| db                 | Image vidéo non compressée |
| dc                 | Image vidéo compressée   |
| pc                 | Modification de la palette           |
| blanc                 | Données audio               |



 

Par exemple, si Stream 0 contient des données audio, les segments de données pour ce flux ont le FOURCC' 00wb'. Si Stream 1 contient une vidéo, les segments de données pour ce flux ont le FOURCC' 01dB’ou' 01dc'. Les segments de données vidéo peuvent également définir de nouvelles entrées de palette pour mettre à jour la palette au cours d’une séquence AVI. Chaque bloc de variation de palette (« xxpc ») contient une structure [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) . Si un flux contient des modifications de palette, définissez l’indicateur **\_ \_ PALCHANGES Video AVISF** dans le membre **dwFlags** de la structure [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) pour ce flux.

Les flux de texte peuvent utiliser des codes à deux caractères arbitraires.

## <a name="avi-index-entries"></a>Entrées d’index AVI

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Index AVI 1,0
</dt> <dd>

Un fragment d’index (« idx1 ») facultatif peut suivre la liste « movi ». L’index contient une liste des segments de données et leur emplacement dans le fichier. Il se compose d’une structure [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) avec des entrées pour chaque segment de données, y compris des segments « Rec ». Si le fichier contient un index, définissez l’indicateur **AVIF \_ HASINDEX** dans le membre **DwFlags** de la structure [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Index AVI 2,0
</dt> <dd>

Un index AVI 2,0 peut apparaître sous la forme d’un segment unique. En guise d’alternative, les segments d’index peuvent être entrelacés dans le bloc « movi ». Si les segments d’index sont placés dans le bloc « movi », un super index contient un index des segments d’index. La structure [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) est la structure de base pour les segments d’index et le Super index. Pour plus d’informations, consultez les *extensions de format de fichier AVI OpenDML*, publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML. (Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)

</dd> </dl>

## <a name="other-data-chunks"></a>Autres segments de données

Les données peuvent être alignées dans un fichier AVI en insérant des blocs « indésirables » en fonction des besoins. Les applications doivent ignorer le contenu d’un bloc « indésirable ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de fichier AVI](avi-file-format.md)
</dt> </dl>

 

 
