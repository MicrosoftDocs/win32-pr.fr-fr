---
description: Référence de fichier RIFF AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Référence de fichier RIFF AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482545"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="82d06-103">Référence de fichier RIFF AVI</span><span class="sxs-lookup"><span data-stu-id="82d06-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="82d06-104">Le format de fichier Microsoft AVI est une spécification de fichier RIFF utilisée avec les applications qui capturent, modifient et lisent des séquences audio-video.</span><span class="sxs-lookup"><span data-stu-id="82d06-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="82d06-105">En général, les fichiers AVI contiennent plusieurs flux de différents types de données.</span><span class="sxs-lookup"><span data-stu-id="82d06-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="82d06-106">La plupart des séquences AVI utilisent à la fois des flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="82d06-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="82d06-107">Une variation simple pour une séquence AVI utilise des données vidéo et ne nécessite pas de flux audio.</span><span class="sxs-lookup"><span data-stu-id="82d06-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="82d06-108">Cette section ne décrit pas les extensions de format de fichier AVI OpenDML.</span><span class="sxs-lookup"><span data-stu-id="82d06-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="82d06-109">Pour plus d’informations sur ces extensions, consultez *extensions de format de fichier AVI OpenDML*, publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML.</span><span class="sxs-lookup"><span data-stu-id="82d06-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="82d06-110">FOURCCs</span><span class="sxs-lookup"><span data-stu-id="82d06-110">FOURCCs</span></span>

<span data-ttu-id="82d06-111">Un code FOURCC (code à quatre caractères) est un entier non signé 32 bits créé par concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="82d06-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="82d06-112">Par exemple, le FOURCC « ABCD » est représenté sur un système de Little-Endian en tant que 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="82d06-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="82d06-113">FOURCCs peut contenir des espaces, « ABC » est donc un FOURCC valide.</span><span class="sxs-lookup"><span data-stu-id="82d06-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="82d06-114">Le format de fichier AVI utilise des Codes FOURCC pour identifier les types de flux, les segments de données, les entrées d’index et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="82d06-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="82d06-115">Format de fichier RIFF</span><span class="sxs-lookup"><span data-stu-id="82d06-115">RIFF File Format</span></span>

<span data-ttu-id="82d06-116">Le format de fichier AVI est basé sur le format de document RIFF (Resource Interchange File Format).</span><span class="sxs-lookup"><span data-stu-id="82d06-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="82d06-117">Un fichier RIFF se compose d’un en-tête RIFF suivi de zéro, une ou plusieurs *listes* et *segments*.</span><span class="sxs-lookup"><span data-stu-id="82d06-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="82d06-118">L’en-tête RIFF se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="82d06-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="82d06-119">où « RIFF » est le littéral de code FOURCC « RIFF », `fileSize` est une valeur de 4 octets qui donne la taille des données dans le fichier et `fileType` est un FourCC qui identifie le type de fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="82d06-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="82d06-120">La valeur de `fileSize` inclut la taille du `fileType` FourCC plus la taille des données qui suivent, mais n’inclut pas la taille du FourCC’riff’ou la taille de `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="82d06-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="82d06-121">Les données de fichier se composent de blocs et de listes, dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="82d06-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="82d06-122">Un segment se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="82d06-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="82d06-123">où `ckID` est un FourCC qui identifie les données contenues dans le bloc, `ckSize` est une valeur de 4 octets qui donne la taille des données dans `ckData` et `ckData` représente zéro, un ou plusieurs octets de données.</span><span class="sxs-lookup"><span data-stu-id="82d06-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="82d06-124">Les données sont toujours complétées à la limite de **mot** la plus proche.</span><span class="sxs-lookup"><span data-stu-id="82d06-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="82d06-125">`ckSize` indique la taille des données valides dans le bloc. elle n’inclut pas le remplissage, la taille `ckID` ou la taille de `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="82d06-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="82d06-126">Une liste se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="82d06-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="82d06-127">où « LIST » est le littéral de code FOURCC « LIST », `listSize` est une valeur de 4 octets qui donne la taille de la liste, `listType` est un code FourCC et `listData` se compose de segments ou de listes, dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="82d06-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="82d06-128">La valeur de `listSize` inclut la taille de `listType` plus la taille de `listData` ; elle n’inclut pas le FourCC’List’ou la taille de `listSize` .</span><span class="sxs-lookup"><span data-stu-id="82d06-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="82d06-129">Le reste de cette section utilise la notation suivante pour décrire les blocs RIFF :</span><span class="sxs-lookup"><span data-stu-id="82d06-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="82d06-130">où la taille de segment est implicite.</span><span class="sxs-lookup"><span data-stu-id="82d06-130">where the chunk size is implicit.</span></span> <span data-ttu-id="82d06-131">À l’aide de cette notation, une liste peut être représentée comme suit :</span><span class="sxs-lookup"><span data-stu-id="82d06-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="82d06-132">Les éléments facultatifs sont placés entre crochets : `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="82d06-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="82d06-133">Forme de formulaire RIFF AVI</span><span class="sxs-lookup"><span data-stu-id="82d06-133">AVI RIFF Form</span></span>

<span data-ttu-id="82d06-134">Les fichiers AVI sont identifiés par le FOURCC « AVI » dans l’en-tête RIFF.</span><span class="sxs-lookup"><span data-stu-id="82d06-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="82d06-135">Tous les fichiers AVI incluent deux blocs de liste obligatoires, qui définissent le format des flux et les données de flux, respectivement.</span><span class="sxs-lookup"><span data-stu-id="82d06-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="82d06-136">Un fichier AVI peut également inclure un segment d’index, qui donne l’emplacement des segments de données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="82d06-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="82d06-137">Un fichier AVI avec ces composants se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="82d06-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="82d06-138">La liste « HDRL » définit le format des données et est le premier bloc de liste requis.</span><span class="sxs-lookup"><span data-stu-id="82d06-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="82d06-139">La liste « movi » contient les données de la séquence AVI et est le deuxième segment de la liste obligatoire.</span><span class="sxs-lookup"><span data-stu-id="82d06-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="82d06-140">La liste « idx1 » contient l’index.</span><span class="sxs-lookup"><span data-stu-id="82d06-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="82d06-141">Les fichiers AVI doivent conserver ces trois composants dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="82d06-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="82d06-142">Les extensions OpenDML définissent un autre type d’index, identifié par le FOURCC « indx ».</span><span class="sxs-lookup"><span data-stu-id="82d06-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="82d06-143">Les listes « HDRL » et « movi » utilisent des sous-segments pour leurs données.</span><span class="sxs-lookup"><span data-stu-id="82d06-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="82d06-144">L’exemple suivant montre le format AVI d’un AVI développé avec les segments nécessaires pour compléter ces listes :</span><span class="sxs-lookup"><span data-stu-id="82d06-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


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



## <a name="avi-main-header"></a><span data-ttu-id="82d06-145">En-tête AVI principal</span><span class="sxs-lookup"><span data-stu-id="82d06-145">AVI Main Header</span></span>

<span data-ttu-id="82d06-146">La liste « HDRL » commence par l’en-tête AVI principal, qui est contenu dans un bloc « AVIH ».</span><span class="sxs-lookup"><span data-stu-id="82d06-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="82d06-147">L’en-tête principal contient des informations globales sur l’ensemble du fichier AVI, telles que le nombre de flux dans le fichier, ainsi que la largeur et la hauteur de la séquence AVI.</span><span class="sxs-lookup"><span data-stu-id="82d06-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="82d06-148">Le segment d’en-tête principal se compose d’une structure [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="82d06-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="82d06-149">En-têtes de flux AVI</span><span class="sxs-lookup"><span data-stu-id="82d06-149">AVI Stream Headers</span></span>

<span data-ttu-id="82d06-150">Une ou plusieurs listes « strl » suivent l’en-tête principal.</span><span class="sxs-lookup"><span data-stu-id="82d06-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="82d06-151">Une liste’strl’est requise pour chaque flux de données.</span><span class="sxs-lookup"><span data-stu-id="82d06-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="82d06-152">Chaque liste « strl » contient des informations sur un flux du fichier et doit contenir un bloc d’en-tête de flux (« Strh ») et un bloc de format de flux (« Strf »).</span><span class="sxs-lookup"><span data-stu-id="82d06-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="82d06-153">En outre, une liste « strl » peut contenir un bloc de données d’en-tête de flux (« StrD ») et un segment de nom de flux (« STRN »).</span><span class="sxs-lookup"><span data-stu-id="82d06-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="82d06-154">Le bloc d’en-tête de flux ('Strh') se compose d’une structure [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .</span><span class="sxs-lookup"><span data-stu-id="82d06-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="82d06-155">Un bloc de format de flux (« Strf ») doit suivre le bloc d’en-tête de flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="82d06-156">Le bloc de format de flux décrit le format des données dans le flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="82d06-157">Les données contenues dans ce segment dépendent du type de flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="82d06-158">Pour les flux vidéo, les informations sont une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , y compris les informations de palette, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="82d06-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="82d06-159">Pour les flux audio, les informations sont une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="82d06-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="82d06-160">Si le segment de données d’en-tête de flux de données (« StrD ») est présent, il suit le bloc de format de flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="82d06-161">Le format et le contenu de ce segment sont définis par le pilote du codec.</span><span class="sxs-lookup"><span data-stu-id="82d06-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="82d06-162">En règle générale, les pilotes utilisent ces informations pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="82d06-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="82d06-163">Les applications qui lisent et écrivent des fichiers AVI n’ont pas besoin d’interpréter ces informations. ils le transfèrent simplement vers et depuis le pilote sous la forme d’un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="82d06-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="82d06-164">Le bloc’STRN’facultatif contient une chaîne de texte se terminant par un caractère null qui décrit le flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="82d06-165">Les en-têtes de flux dans la liste « HDRL » sont associés aux données de flux dans la liste « movi » en fonction de l’ordre des segments « strl ».</span><span class="sxs-lookup"><span data-stu-id="82d06-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="82d06-166">Le premier segment « strl » s’applique au flux 0, le deuxième s’applique à Stream 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="82d06-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="82d06-167">Données de flux (liste « movi »)</span><span class="sxs-lookup"><span data-stu-id="82d06-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="82d06-168">Le fait de suivre les informations d’en-tête est une liste « movi » qui contient les données réelles dans les flux, c’est-à-dire les images vidéo et les échantillons audio.</span><span class="sxs-lookup"><span data-stu-id="82d06-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="82d06-169">Les segments de données peuvent résider directement dans la liste « movi », ou ils peuvent être regroupés dans des listes « Rec ».</span><span class="sxs-lookup"><span data-stu-id="82d06-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="82d06-170">Le regroupement « Rec » implique que les segments groupés doivent être lus à partir du disque en une seule fois et sont destinés aux fichiers qui sont entrelacés pour être lus à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="82d06-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="82d06-171">Le FOURCC qui identifie chaque segment de données se compose d’un numéro de flux à deux chiffres suivi d’un code à deux caractères qui définit le type d’informations dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="82d06-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="82d06-172">Code à deux caractères</span><span class="sxs-lookup"><span data-stu-id="82d06-172">Two-character code</span></span> | <span data-ttu-id="82d06-173">Description</span><span class="sxs-lookup"><span data-stu-id="82d06-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="82d06-174">db</span><span class="sxs-lookup"><span data-stu-id="82d06-174">db</span></span>                 | <span data-ttu-id="82d06-175">Image vidéo non compressée</span><span class="sxs-lookup"><span data-stu-id="82d06-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="82d06-176">dc</span><span class="sxs-lookup"><span data-stu-id="82d06-176">dc</span></span>                 | <span data-ttu-id="82d06-177">Image vidéo compressée</span><span class="sxs-lookup"><span data-stu-id="82d06-177">Compressed video frame</span></span>   |
| <span data-ttu-id="82d06-178">pc</span><span class="sxs-lookup"><span data-stu-id="82d06-178">pc</span></span>                 | <span data-ttu-id="82d06-179">Modification de la palette</span><span class="sxs-lookup"><span data-stu-id="82d06-179">Palette change</span></span>           |
| <span data-ttu-id="82d06-180">blanc</span><span class="sxs-lookup"><span data-stu-id="82d06-180">wb</span></span>                 | <span data-ttu-id="82d06-181">Données audio</span><span class="sxs-lookup"><span data-stu-id="82d06-181">Audio data</span></span>               |



 

<span data-ttu-id="82d06-182">Par exemple, si Stream 0 contient des données audio, les segments de données pour ce flux ont le FOURCC' 00wb'.</span><span class="sxs-lookup"><span data-stu-id="82d06-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="82d06-183">Si Stream 1 contient une vidéo, les segments de données pour ce flux ont le FOURCC' 01dB’ou' 01dc'.</span><span class="sxs-lookup"><span data-stu-id="82d06-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="82d06-184">Les segments de données vidéo peuvent également définir de nouvelles entrées de palette pour mettre à jour la palette au cours d’une séquence AVI.</span><span class="sxs-lookup"><span data-stu-id="82d06-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="82d06-185">Chaque bloc de variation de palette (« xxpc ») contient une structure [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) .</span><span class="sxs-lookup"><span data-stu-id="82d06-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="82d06-186">Si un flux contient des modifications de palette, définissez l’indicateur **\_ \_ PALCHANGES Video AVISF** dans le membre **dwFlags** de la structure [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="82d06-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="82d06-187">Les flux de texte peuvent utiliser des codes à deux caractères arbitraires.</span><span class="sxs-lookup"><span data-stu-id="82d06-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="82d06-188">Entrées d’index AVI</span><span class="sxs-lookup"><span data-stu-id="82d06-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="82d06-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Index AVI 1,0</span><span class="sxs-lookup"><span data-stu-id="82d06-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="82d06-190">Un fragment d’index (« idx1 ») facultatif peut suivre la liste « movi ».</span><span class="sxs-lookup"><span data-stu-id="82d06-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="82d06-191">L’index contient une liste des segments de données et leur emplacement dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="82d06-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="82d06-192">Il se compose d’une structure [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) avec des entrées pour chaque segment de données, y compris des segments « Rec ».</span><span class="sxs-lookup"><span data-stu-id="82d06-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="82d06-193">Si le fichier contient un index, définissez l’indicateur **AVIF \_ HASINDEX** dans le membre **DwFlags** de la structure [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="82d06-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82d06-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Index AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="82d06-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="82d06-195">Un index AVI 2,0 peut apparaître sous la forme d’un segment unique.</span><span class="sxs-lookup"><span data-stu-id="82d06-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="82d06-196">En guise d’alternative, les segments d’index peuvent être entrelacés dans le bloc « movi ».</span><span class="sxs-lookup"><span data-stu-id="82d06-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="82d06-197">Si les segments d’index sont placés dans le bloc « movi », un super index contient un index des segments d’index.</span><span class="sxs-lookup"><span data-stu-id="82d06-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="82d06-198">La structure [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) est la structure de base pour les segments d’index et le Super index.</span><span class="sxs-lookup"><span data-stu-id="82d06-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="82d06-199">Pour plus d’informations, consultez les *extensions de format de fichier AVI OpenDML*, publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML.</span><span class="sxs-lookup"><span data-stu-id="82d06-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="82d06-200">(Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="82d06-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="82d06-201">Autres segments de données</span><span class="sxs-lookup"><span data-stu-id="82d06-201">Other Data Chunks</span></span>

<span data-ttu-id="82d06-202">Les données peuvent être alignées dans un fichier AVI en insérant des blocs « indésirables » en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="82d06-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="82d06-203">Les applications doivent ignorer le contenu d’un bloc « indésirable ».</span><span class="sxs-lookup"><span data-stu-id="82d06-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82d06-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82d06-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d06-205">Format de fichier AVI</span><span class="sxs-lookup"><span data-stu-id="82d06-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
