---
description: cette spécification décrit la structure des fichiers exécutables (image) et des fichiers objets sous la famille de systèmes d’exploitation Windows. Ces fichiers sont respectivement appelés fichiers exécutables portables (PE, Portable Executable) et COFF (Common Object File Format).
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Format PE
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: f20431f7f56c64d5d430c9992da72ea4331cbf21
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812194"
---
# <a name="pe-format"></a>Format PE

cette spécification décrit la structure des fichiers exécutables (image) et des fichiers objets sous la famille de systèmes d’exploitation Windows. Ces fichiers sont respectivement appelés fichiers exécutables portables (PE, Portable Executable) et COFF (Common Object File Format).

> [!Note]  
> ce document est fourni pour faciliter le développement d’outils et d’applications pour Windows, mais il n’est pas garanti qu’il s’agit d’une spécification complète à tous égards. Microsoft se réserve le droit de modifier ce document sans préavis.

Cette révision du fichier exécutable portable Microsoft et de la spécification de format de fichier objet commun remplace toutes les révisions précédentes de cette spécification.

## <a name="general-concepts"></a>Concepts généraux

ce document spécifie la structure des fichiers exécutables (image) et des fichiers objets sous la famille de systèmes d’exploitation Microsoft Windows. Ces fichiers sont respectivement appelés fichiers exécutables portables (PE, Portable Executable) et COFF (Common Object File Format). Le nom « exécutable portable » fait référence au fait que le format n’est pas spécifique à l’architecture.

Certains concepts qui s’affichent tout au long de cette spécification sont décrits dans le tableau suivant :

| Name                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificat d’attribut <br/> | Certificat utilisé pour associer des instructions vérifiables à une image. Plusieurs instructions vérifiables différentes peuvent être associées à un fichier ; l’une des plus utiles est une déclaration d’un fabricant de logiciels qui indique le niveau de synthèse du message de l’image. Un résumé de message est semblable à une somme de contrôle, à ceci près qu’il est extrêmement difficile à falsifier. Par conséquent, il est très difficile de modifier un fichier pour qu’il ait le même Résumé de message que le fichier d’origine. L’instruction peut être vérifiée par le fabricant en utilisant des schémas de chiffrement à clé publique ou privée. Ce document décrit en détail les certificats d’attribut autres que pour permettre leur insertion dans des fichiers image. <br/> |
| horodatage <br/>       | Horodatage utilisé à des fins différentes à plusieurs emplacements dans un fichier PE ou COFF. Dans la plupart des cas, le format de chaque tampon est le même que celui utilisé par les fonctions d’heure de la bibliothèque Runtime C. Pour obtenir des exceptions, consultez la Descriptor de la \_ reproduction de type de débogage d’image \_ \_ en [type de débogage](#debug-type). Si la valeur de tampon est 0 ou 0xFFFFFFFF, elle ne représente pas un horodatage réel ou explicite. <br/>                                                                                                                                                                                                                                                                                                                                            |
| pointeur de fichier <br/>          | Emplacement d’un élément dans le fichier lui-même, avant d’être traité par l’éditeur de liens (dans le cas des fichiers objets) ou le chargeur (dans le cas des fichiers image). En d’autres termes, il s’agit d’une position dans le fichier telle qu’elle est stockée sur le disque. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| éditeur de liens <br/>                | Référence à l’éditeur de liens fourni avec Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| fichier objet <br/>           | Fichier donné comme entrée à l’éditeur de liens. L’éditeur de liens produit un fichier image qui, à son tour, est utilisé comme entrée par le chargeur. Le terme « fichier objet » n’implique pas nécessairement une connexion à la programmation orientée objet. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| réservé, doit avoir la valeur 0 <br/>   | Description d’un champ qui indique que la valeur du champ doit être égale à zéro pour les générateurs et que les consommateurs doivent ignorer le champ. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Adresse virtuelle relative (RVA) <br/>                   | Dans un fichier image, il s’agit de l’adresse d’un élément après son chargement en mémoire, avec l’adresse de base du fichier image soustrait de celui-ci. L’adresse RVA d’un élément diffère presque toujours de sa position dans le fichier sur le disque (pointeur de fichier). <br/> Dans un fichier objet, une adresse RVA est moins explicite, car les emplacements de mémoire ne sont pas assignés. Dans ce cas, un RVA serait une adresse dans une section (décrite plus loin dans ce tableau), à laquelle un réadressage est appliqué ultérieurement lors de la liaison. Par souci de simplicité, un compilateur doit simplement définir la première adresse RVA de chaque section sur zéro. <br/>                                                                                                                                         |
| section <br/>               | Unité de base de code ou de données dans un fichier PE ou COFF. Par exemple, tout le code d’un fichier objet peut être combiné dans une section unique ou (selon le comportement du compilateur) chaque fonction peut occuper sa propre section. Avec plus de sections, il y a plus de surcharge de fichiers, mais l’éditeur de liens est en mesure de lier le code de manière plus sélective. Une section est similaire à un segment dans l’architecture Intel 8086. Toutes les données brutes d’une section doivent être chargées de façon contiguë. En outre, un fichier image peut contenir un certain nombre de sections, telles que. TLS ou. reloc, qui ont des objectifs spéciaux. <br/>                                                                                                                                                                      |
| Adresse virtuelle (VA) <br/>                    | Identique à RVA, sauf que l’adresse de base du fichier image n’est pas soustraite. l’adresse est appelée VA car Windows crée un espace de va distinct pour chaque processus, indépendamment de la mémoire physique. Pour presque tous les besoins, un VA doit être considéré comme une seule adresse. Un VA n’est pas aussi prévisible en tant que RVA car le chargeur risque de ne pas charger l’image à son emplacement préféré. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Vue d’ensemble

La liste suivante décrit le format exécutable de Microsoft PE, avec la base de l’en-tête d’image en haut. La section de l’en-tête EXE compatible MS-DOS 2,0 passant à la section inutilisée juste avant l’en-tête PE est la section MS-DOS 2,0 et est utilisée uniquement pour la compatibilité MS-DOS.

-   En-tête EXE compatible MS-DOS 2,0
-   unused
-   Identificateur OEM

    Informations OEM

    Décalage vers l’en-tête PE

-   Programme stub MS-DOS 2,0 et table de réadressage

-   unused

-   En-tête PE (aligné sur la limite de 8 octets)

-   En-têtes de section
-   Pages d’image :

    importer des informations

    exporter les informations

    réadressages de base

    informations sur les ressources

La liste suivante décrit le format de module d’objets COFF Microsoft :

-   En-tête Microsoft COFF
-   En-têtes de section
-   Données brutes :

    code

    data

    informations de débogage

    réadressages

## <a name="file-headers"></a>En-têtes de fichier

- [Stub MS-DOS (image uniquement)](#ms-dos-stub-image-only)
- [Signature (image uniquement)](#signature-image-only)
- [En-tête de fichier COFF (objet et image)](#coff-file-header-object-and-image)
  - [Types d’ordinateurs](#machine-types)
  - [Caractéristiques](#characteristics)
- [En-tête facultatif (image uniquement)](#optional-header-image-only)
  - [Champs standard d’en-tête facultatifs (image uniquement)](#optional-header-standard-fields-image-only)
  - [Champs d’en-tête facultatifs Windows-Specific (image uniquement)](#optional-header-windows-specific-fields-image-only)
  - [Répertoires de données d’en-tête facultatifs (image uniquement)](#optional-header-data-directories-image-only)

L’en-tête de fichier PE se compose d’un stub Microsoft MS-DOS, de la signature PE, de l’en-tête de fichier COFF et d’un en-tête facultatif. Un en-tête de fichier objet COFF se compose d’un en-tête de fichier COFF et d’un en-tête facultatif. Dans les deux cas, les en-têtes de fichier sont immédiatement suivis par des en-têtes de section.

### <a name="ms-dos-stub-image-only"></a>Stub MS-DOS (image uniquement)

Le stub MS-DOS est une application valide qui s’exécute sous MS-DOS. Elle est placée au début de l’image EXE. L’éditeur de liens place un stub par défaut ici, qui imprime le message « ce programme ne peut pas être exécuté en mode DOS » lorsque l’image est exécutée dans MS-DOS. L’utilisateur peut spécifier un autre stub à l’aide de l’option/STUB de l’éditeur de liens.

À l’emplacement 0x3C, le stub a le décalage de fichier par rapport à la signature PE. ces informations permettent à Windows d’exécuter correctement le fichier image, même s’il dispose d’un stub MS-DOS. Ce décalage de fichier est placé à l’emplacement 0x3C lors de la liaison.

### <a name="signature-image-only"></a>Signature (image uniquement)

Une fois que le stub MS-DOS, au décalage de fichier spécifié à l’offset 0x3C, est une signature de 4 octets qui identifie le fichier en tant que fichier image au format PE. Cette signature est « PE \\ 0 \\ 0 » (les lettres « P » et « E » suivies de deux octets null).

### <a name="coff-file-header-object-and-image"></a>En-tête de fichier COFF (objet et image)

Au début d’un fichier objet, ou immédiatement après la signature d’un fichier image, est un en-tête de fichier COFF standard au format suivant. notez que le chargeur de Windows limite le nombre de sections à 96.

| Offset         | Taille          | Champ                            | Description                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Machine <br/>              | Numéro qui identifie le type d’ordinateur cible. Pour plus d’informations, consultez [types de machines](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Nombre de sections. Cela indique la taille de la table de la section, qui suit immédiatement les en-têtes. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | 32 bits de poids faible du nombre de secondes écoulées depuis 00:00 le 1er janvier 1970 (valeur t Runtime C \_ ), qui indique le moment où le fichier a été créé. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | Offset de fichier de la table de symboles COFF, ou zéro si aucune table de symboles COFF n’est présente. Cette valeur doit être égale à zéro pour une image, car les informations de débogage COFF sont dépréciées. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Nombre d’entrées dans la table de symboles. Ces données peuvent être utilisées pour localiser la table de chaînes, qui suit immédiatement la table de symboles. Cette valeur doit être égale à zéro pour une image, car les informations de débogage COFF sont dépréciées. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Taille de l’en-tête facultatif, qui est requis pour les fichiers exécutables, mais pas pour les fichiers objets. Cette valeur doit être égale à zéro pour un fichier objet. Pour obtenir une description du format d’en-tête, consultez l' [en-tête facultatif (image uniquement)](#optional-header-image-only). <br/> |
| 18 <br/> | 2 <br/> | Caractéristiques <br/>      | Indicateurs qui indiquent les attributs du fichier. Pour obtenir des valeurs d’indicateur spécifiques, consultez [caractéristiques](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Types d’ordinateurs

Le champ ordinateur a l’une des valeurs suivantes, qui spécifient le type de processeur. Un fichier image ne peut être exécuté que sur l’ordinateur spécifié ou sur un système qui émule l’ordinateur spécifié.

| Constante                                    | Valeur              | Description                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| \_ordinateur de fichier image \_ \_ inconnu <br/>   | 0x0 <br/>    | Le contenu de ce champ est supposé être applicable à n’importe quel type de machine <br/> |
| \_Ordinateur de fichier image \_ \_ AM33 <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| \_Machine de fichier image \_ \_ amd64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| fichier IMAGE bras de l' \_ \_ ordinateur \_ <br/>       | 0x1c0 <br/>  | Little endian ARM <br/>                                                           |
| \_Ordinateur de fichier image \_ \_ ARM64 <br/>     | 0xaa64 <br/> | ARM64 Little endian <br/>                                                         |
| \_ordinateur de fichier image \_ \_ ARMNT <br/>     | 0x1c4 <br/>  | Thumb ARM-2 Little endian <br/>                                                   |
| \_fichier d' \_ image \_ EBC machine <br/>       | 0xebc <br/>  | Code d’octet EFI <br/>                                                               |
| \_Fichier image \_ ordinateur \_ i386 <br/>      | 0x14c <br/>  | Processeurs Intel 386 ou ultérieurs et processeurs compatibles <br/>                     |
| \_Machine de fichier image \_ \_ ia64 <br/>      | 0x200 <br/>  | Famille de processeurs Intel Itanium <br/>                                              |
| \_Ordinateur de fichier image \_ \_ m32r <br/>      | 0x9041 <br/> | Mitsubishi M32R Little endian <br/>                                               |
| \_Ordinateur de fichier image \_ \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| \_ordinateur de fichier image \_ \_ MIPSFPU <br/>   | 0x366 <br/>  | MIPS avec FPU <br/>                                                               |
| \_Ordinateur de fichier image \_ \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 avec FPU <br/>                                                             |
| \_fichier image \_ ordinateur \_ powerpc <br/>   | 0x1f0 <br/>  | Petit-endian Power PC <br/>                                                      |
| \_ordinateur de fichier image \_ \_ POWERPCFP <br/> | 0x1f1 <br/>  | Power PC avec prise en charge de la virgule flottante <br/>                                        |
| \_Ordinateur de fichier image \_ \_ R4000 <br/>     | 0x166 <br/>  | Little endian MIPS <br/>                                                          |
| \_Ordinateur de fichier image \_ \_ RISCV32 <br/>   | 0x5032 <br/> | Espace d’adressage RISC-V 32 bits <br/>                                                 |
| \_Ordinateur de fichier image \_ \_ RISCV64 <br/>   | 0x5064 <br/> | Espace d’adressage RISC-V 64 bits <br/>                                                 |
| \_Ordinateur de fichier image \_ \_ RISCV128 <br/>  | 0x5128 <br/> | Espace d’adressage RISC-V 128 bits <br/>                                                |
| \_Ordinateur du fichier image \_ \_ SH3 <br/>       | 0x1a2 <br/>  | SH3 d’Hitachi <br/>                                                                 |
| \_Ordinateur de fichier image \_ \_ SH3DSP <br/>    | 0x1a3 <br/>  | DSP SH3 DSP <br/>                                                             |
| \_Machine fichier \_ image \_ sh4 <br/>       | 0x1a6 <br/>  | HITACHI SH4 <br/>                                                                 |
| \_Ordinateur de fichier image \_ \_ SH5 <br/>       | 0x1a8 <br/>  | Hitachi SH5 <br/>                                                                 |
| curseur de l' \_ ordinateur du fichier image \_ \_ <br/>     | 0x1c2 <br/>  | Thumb <br/>                                                                       |
| \_Ordinateur de fichier image \_ \_ WCEMIPSV2 <br/> | 0x169 <br/>  | minimum de MIPS-endian WCE v2 <br/>                                                   |

#### <a name="characteristics"></a>Caractéristiques

Le champ caractéristiques contient des indicateurs qui indiquent les attributs de l’objet ou du fichier image. Les indicateurs suivants sont actuellement définis :

| Indicateur                                                 | Valeur              | Description                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fichier image \_ des réadressages \_ supprimé <br/>            | 0x0001 <br/> | Image only, Windows CE et Microsoft Windows NT et versions ultérieures. Cela indique que le fichier ne contient pas de réadressages de base et doit donc être chargé à son adresse de base préférée. Si l’adresse de base n’est pas disponible, le chargeur signale une erreur. Le comportement par défaut de l’éditeur de liens consiste à supprimer les réadressages de base des fichiers exécutables (EXE). <br/> |
| \_ \_ image exécutable du fichier \_ image <br/>           | 0x0002 <br/> | Image uniquement. Cela indique que le fichier image est valide et peut être exécuté. Si cet indicateur n’est pas défini, il indique une erreur de l’éditeur de liens. <br/>                                                                                                                                                                                                                          |
| \_lignes de fichier image \_ \_ \_ tronquées <br/>        | 0x0004 <br/> | Les numéros de ligne COFF ont été supprimés. Cet indicateur est déconseillé et doit être égal à zéro. <br/>                                                                                                                                                                                                                                                                       |
| \_fichier image \_ local \_ Syms \_ supprimé <br/>       | 0x0008 <br/> | Les entrées de table de symboles COFF pour les symboles locaux ont été supprimées. Cet indicateur est déconseillé et doit être égal à zéro. <br/>                                                                                                                                                                                                                                             |
| fichier IMAGE de la \_ \_ \_ suppression agressive WS \_ <br/>        | 0x0010 <br/> | Obsolète. Supprimer le jeu de travail de manière agressive. cet indicateur est déconseillé pour Windows 2000 et versions ultérieures et doit être égal à zéro. <br/>                                                                                                                                                                                                                                          |
| prise \_ en \_ \_ charge d’adresses volumineuses dans un fichier image \_ <br/>      | 0x0020 <br/> | L’application peut gérer des adresses > 2 Go. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Cet indicateur est réservé à une utilisation ultérieure. <br/>                                                                                                                                                                                                                                                                                                                  |
| \_octets du fichier image inversé ( \_ \_ \_ Lo) <br/>         | 0x0080 <br/> | Little endian : le bit le moins significatif (LSB) précède le bit le plus significatif (MSB) en mémoire. Cet indicateur est déconseillé et doit être égal à zéro. <br/>                                                                                                                                                                                                          |
| \_Ordinateur de fichier image \_ 32 bits \_ <br/>              | 0x0100 <br/> | L’ordinateur est basé sur une architecture de type 32 bits. <br/>                                                                                                                                                                                                                                                                                                        |
| débogage du \_ fichier image \_ \_ supprimé <br/>             | 0x0200 <br/> | Les informations de débogage sont supprimées du fichier image. <br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ \_ exécution \_ de l’échange amovible du \_ fichier image <br/> | 0x0400 <br/> | Si l’image se trouve sur un support amovible, chargez-la entièrement et copiez-la dans le fichier d’échange. <br/>                                                                                                                                                                                                                                                                        |
| \_fichier image \_ NET \_ exécuté \_ à partir de l' \_ échange <br/>        | 0x0800 <br/> | Si l’image se trouve sur un support réseau, chargez-la entièrement et copiez-la dans le fichier d’échange. <br/>                                                                                                                                                                                                                                                                          |
| \_système de fichiers image \_ <br/>                      | 0x1000 <br/> | Le fichier image est un fichier système, et non un programme utilisateur. <br/>                                                                                                                                                                                                                                                                                                   |
| \_dll du fichier image \_ <br/>                         | 0x2000 <br/> | Le fichier image est une bibliothèque de liens dynamiques (DLL). Ces fichiers sont considérés comme des fichiers exécutables à presque tous les fins, bien qu’ils ne puissent pas être exécutés directement. <br/>                                                                                                                                                                                              |
| \_fichier image \_ vers le haut \_ \_ uniquement <br/>            | 0x4000 <br/> | Le fichier doit être exécuté uniquement sur un ordinateur monoprocesseur. <br/>                                                                                                                                                                                                                                                                                                 |
| octets du fichier IMAGE en \_ \_ arrière- \_ \_ haut <br/>         | 0x8000 <br/> | Big endian : le MSB précède le LSB en mémoire. Cet indicateur est déconseillé et doit être égal à zéro. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>En-tête facultatif (image uniquement)

Chaque fichier image possède un en-tête facultatif qui fournit des informations au chargeur. Cet en-tête est facultatif dans le sens où certains fichiers (plus particulièrement les fichiers objets) n’en ont pas. Pour les fichiers image, cet en-tête est obligatoire. Un fichier objet peut avoir un en-tête facultatif, mais cet en-tête n’a généralement aucune fonction dans un fichier objet, sauf pour augmenter sa taille.

Notez que la taille de l’en-tête facultatif n’est pas fixe. Le champ **SizeOfOptionalHeader** de l’en-tête COFF doit être utilisé pour valider le fait qu’une sonde dans le fichier d’un répertoire de données particulier n’excède pas **SizeOfOptionalHeader**. Pour plus d’informations, consultez [en-tête de fichier COFF (objet et image)](#coff-file-header-object-and-image).

Le champ **NumberOfRvaAndSizes** de l’en-tête facultatif doit également être utilisé pour s’assurer qu’aucune sonde pour une entrée spécifique d’un répertoire de données ne dépasse l’en-tête facultatif. En outre, il est important de valider l’en-tête facultatif nombre magique pour la compatibilité de format.

Le nombre magique d’en-tête facultatif détermine si une image est un fichier exécutable PE32 ou PE32 +.

| Nombre magique      | Format PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32 + <br/> |

Les images PE32 + permettent d’obtenir un espace d’adressage de 64 bits tout en limitant la taille de l’image à 2 gigaoctets. Les autres modifications apportées à PE32 et sont traitées dans leurs sections respectives.

L’en-tête facultatif lui-même a trois parties principales.

| Décalage (PE32/PE32 +) | Taille (PE32/PE32 +)    | Partie d’en-tête                         | Description                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Champs standard <br/>         | Champs définis pour toutes les implémentations de COFF, y compris UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | champs spécifiques à Windows <br/> | champs supplémentaires pour prendre en charge des fonctionnalités spécifiques de Windows (par exemple, les sous-systèmes). <br/>                                                                              |
| 96/112 <br/>  | Variable <br/> | Répertoires de données <br/>        | Paires adresse/taille pour les tables spéciales qui se trouvent dans le fichier image et sont utilisées par le système d’exploitation (par exemple, la table d’importation et la table d’exportation). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Champs standard d’en-tête facultatifs (image uniquement)

Les huit premiers champs de l’en-tête facultatif sont des champs standard définis pour chaque implémentation de COFF. Ces champs contiennent des informations générales qui sont utiles pour le chargement et l’exécution d’un fichier exécutable. Elles sont inchangées pour le format PE32 +.

| Offset         | Taille          | Champ                               | Description                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Commande magique <br/>                   | Entier non signé qui identifie l’état du fichier image. Le nombre le plus courant est 0x10B, qui l’identifie en tant que fichier exécutable normal. 0x107 l’identifie comme une image ROM et 0x20B l’identifie comme un exécutable PE32 +. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | Numéro de version principale de l’éditeur de liens. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | Numéro de version mineure de l’éditeur de liens. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | La taille de la section de code (texte) ou la somme de toutes les sections de code s’il y a plusieurs sections. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | Taille de la section des données initialisées, ou somme de toutes ces sections s’il y a plusieurs sections de données. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | Taille de la section de données non initialisées (BSS) ou somme de toutes ces sections s’il existe plusieurs sections BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | Adresse du point d’entrée par rapport à la base de l’image lorsque le fichier exécutable est chargé en mémoire. Pour les images de programme, il s’agit de l’adresse de départ. Pour les pilotes de périphérique, il s’agit de l’adresse de la fonction d’initialisation. Un point d’entrée est facultatif pour les dll. Si aucun point d’entrée n’est présent, ce champ doit être égal à zéro. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Adresse relative à la base de l’image de la section de début de code lorsqu’elle est chargée en mémoire. <br/>                                                                                                                                                                                                                    |

PE32 contient ce champ supplémentaire, qui est absent dans PE32 +, à la suite de BaseOfCode.

| Offset         | Taille          | Champ                  | Description                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Adresse relative à la base de l’image de la section de début de données lorsqu’elle est chargée en mémoire. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Champs d’en-tête facultatifs Windows-Specific (image uniquement)

Les 21 champs suivants sont une extension du format d’en-tête facultatif COFF. Ils contiennent des informations supplémentaires requises par l’éditeur de liens et le chargeur dans Windows.

| Décalage (PE32/PE32 +) | Taille (PE32/PE32 +) | Champ                                   | Description                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | Adresse par défaut du premier octet de l’image en cas de chargement en mémoire ; doit être un multiple de 64 K. La valeur par défaut des dll est 0x10000000. la valeur par défaut pour Windows CE exe est 0x00010000. la valeur par défaut pour Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 et Windows Me est 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | Alignement (en octets) des sections quand elles sont chargées en mémoire. Elle doit être supérieure ou égale à assigne FileAlignment. La valeur par défaut correspond à la taille de page de l’architecture. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | Facteur d’alignement (en octets) utilisé pour aligner les données brutes des sections du fichier image. La valeur doit être une puissance de 2 comprise entre 512 et 64 K inclus. La valeur par défaut est 512. Si la valeur de alignement de section est inférieure à la taille de page de l’architecture, assigne FileAlignment doit correspondre à alignement de section. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | Numéro de version principale du système d’exploitation nécessaire. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | Numéro de version mineure du système d’exploitation nécessaire. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | Numéro de version principale de l’image. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | Numéro de version mineure de l’image. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | Numéro de version principale du sous-système. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | Numéro de version mineure du sous-système. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Réservé, doit être égal à zéro. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Taille (en octets) de l’image, y compris tous les en-têtes, lorsque l’image est chargée en mémoire. Il doit s’agir d’un multiple de alignement de section. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | La taille combinée d’un stub MS-DOS, d’un en-tête PE et d’en-têtes de section est arrondie à un multiple de assigne FileAlignment. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | EEPROM <br/>                    | Somme de contrôle du fichier image. L’algorithme de calcul de la somme de contrôle est incorporé dans IMAGHELP.DLL. les éléments suivants sont vérifiés pour la validation au moment du chargement : tous les pilotes, toute dll chargée au moment du démarrage et toute dll chargée dans un processus de Windows critique. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | Sous-système nécessaire pour exécuter cette image. pour plus d’informations, consultez [Windows sous-système](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Pour plus d’informations, consultez caractéristiques de la [dll](#dll-characteristics) plus loin dans cette spécification. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | Taille de la pile à réserver. Seul SizeOfStackCommit est validé ; le reste est mis à disposition une page à la fois jusqu’à ce que la taille de réserve soit atteinte. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | Taille de la pile à commiter. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | Taille de l’espace du tas local à réserver. Seul SizeOfHeapCommit est validé ; le reste est mis à disposition une page à la fois jusqu’à ce que la taille de réserve soit atteinte. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | Taille de l’espace du tas local à commiter. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Réservé, doit être égal à zéro. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | Nombre d’entrées de répertoire de données dans le reste de l’en-tête facultatif. Chacune décrit un emplacement et une taille. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Windows Sous-système

les valeurs suivantes définies pour le champ sous-système de l’en-tête facultatif déterminent le sous-système de Windows (le cas échéant) requis pour exécuter l’image.

| Constante                                                  | Valeur          | Description                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| \_sous-système d’image \_ inconnu <br/>                     | 0 <br/>  | Sous-système inconnu <br/>                                 |
| \_sous-système d’image \_ natif <br/>                      | 1 <br/>  | pilotes de périphériques et processus de Windows natif <br/>          |
| \_GUI Windows de sous-système d’images \_ \_ <br/>                | 2 <br/>  | sous-système de l’interface graphique utilisateur (GUI) Windows <br/> |
| \_sous-système d’image \_ Windows \_ Cui <br/>                | 3 <br/>  | sous-système de caractères Windows <br/>                      |
| \_Sous-système d’images \_ OS2 \_ Cui <br/>                    | 5 <br/>  | Sous-système du système d’exploitation/2 caractères <br/>                         |
| \_sous-système \_ POSIX d’image \_ Cui <br/>                  | 7 <br/>  | Sous-système de caractères POSIX <br/>                        |
| \_sous-système d’image \_ \_ Windows natif <br/>             | 8 <br/>  | Pilote Win9x natif <br/>                                  |
| \_ \_ \_ GUI Windows ce sous-système d’images \_ <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_application EFI du sous-système d’images \_ \_ <br/>            | 10 <br/> | Une application Extensible Firmware Interface (EFI) <br/>   |
| \_pilote du service de \_ démarrage EFI du \_ \_ sous-système d’images \_ <br/> | 11 <br/> | Pilote EFI avec les services de démarrage <br/>                     |
| \_ \_ pilote d’exécution EFI \_ du sous-système \_ d’images <br/>       | 12 <br/> | Pilote EFI avec des services d’exécution <br/>                 |
| \_sous-système d’image \_ \_ ROM EFI <br/>                    | 13 <br/> | Une image ROM EFI <br/>                                     |
| \_Xbox du sous-système d’images \_ <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| \_sous-système d’images- \_ \_ application de démarrage Windows \_ <br/>  | 16 <br/> | Windows l’application de démarrage. <br/>                            |

##### <a name="dll-characteristics"></a>Caractéristiques de la DLL

Les valeurs suivantes sont définies pour le champ DllCharacteristics de l’en-tête facultatif.

| Constante                                                             | Valeur              | Description                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Réservé, doit être égal à zéro. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Réservé, doit être égal à zéro. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Réservé, doit être égal à zéro. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Réservé, doit être égal à zéro. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ d' \_ entropie élevée \_ <br/>             | 0x0020 <br/> | L’image peut gérer un espace d’adressage virtuel 64 bits d’entropie élevé. <br/>                               |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> \_base dynamique <br/>    | 0x0040 <br/> | La DLL peut être déplacée au moment du chargement. <br/>                                                          |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> FORCER \_ l’intégrité <br/> | 0x0080 <br/> | Les contrôles d’intégrité du code sont appliqués. <br/>                                                         |
| IMAGE \_ DLLCHARACTERISTICS\_ <br/> \_compatibilité NX <br/>       | 0x0100 <br/> | L’image est compatible avec NX. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ aucune \_ isolation <br/>                | 0x0200 <br/> | Prise en charge de l’isolement, mais n’isolez pas l’image. <br/>                                              |
| IMAGE \_ DLLCHARACTERISTICS \_ non \_ SEH <br/>                      | 0x0400 <br/> | n’utilise pas la gestion des exceptions structurées (SE). aucun gestionnaire de SE ne peut être appelé dans cette image. <br/> |
| IMAGE \_ DLLCHARACTERISTICS \_ aucune \_ liaison <br/>                     | 0x0800 <br/> | Ne liez pas l’image. <br/>                                                                      |
| IMAGE \_ DLLCHARACTERISTICS \_ APPCONTAINER <br/>                  | 0x1000 <br/> | L’image doit s’exécuter dans un AppContainer. <br/>                                                      |
| \_ \_ pilote WDM image \_ DLLCHARACTERISTICS <br/>                  | 0x2000 <br/> | Pilote WDM. <br/>                                                                               |
| IMAGE \_ DLLCHARACTERISTICS \_ Guard \_ CF <br/>                     | 0x4000 <br/> | l’Image prend en charge le contrôle Flow Guard. <br/>                                                          |
| prise en charge d’IMAGE \_ DLLCHARACTERISTICS \_ Terminal \_ Server \_ <br/>      | 0x8000 <br/> | Prise en charge Terminal Server. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Répertoires de données d’en-tête facultatifs (image uniquement)

chaque répertoire de données fournit l’adresse et la taille d’une table ou d’une chaîne que Windows utilise. Ces entrées de répertoire de données sont toutes chargées dans la mémoire afin que le système puisse les utiliser au moment de l’exécution. Un répertoire de données est un champ de 8 octets qui contient la déclaration suivante :

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

Le premier champ, VirtualAddress, est en fait l’adresse RVA de la table. L’adresse RVA est l’adresse de la table par rapport à l’adresse de base de l’image lorsque la table est chargée. Le deuxième champ donne la taille en octets. Les répertoires de données, qui forment la dernière partie de l’en-tête facultatif, sont répertoriés dans le tableau suivant.

Notez que le nombre de répertoires n’est pas fixe. Avant de rechercher un répertoire spécifique, vérifiez le champ NumberOfRvaAndSizes dans l’en-tête facultatif.

En outre, ne partez pas du principe que les RVA de cette table pointent vers le début d’une section ou que les sections qui contiennent des tables spécifiques ont des noms spécifiques.

| Décalage (PE/PE32 +)   | Taille          | Champ                               | Description                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Exporter une table <br/>            | L’adresse et la taille de la table d’exportation. Pour plus d’informations [, consultez la section. edata (image uniquement)](#the-edata-section-image-only). <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importer une table <br/>            | L’adresse et la taille de la table d’importation. Pour plus d’informations, consultez [la section. idata](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Table de ressources <br/>          | L’adresse et la taille de la table de ressources. Pour plus d’informations, consultez [la section. rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Table d’exceptions <br/>         | L’adresse et la taille de la table d’exception. Pour plus d’informations, consultez [la section. pdata](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Table de certificats <br/>       | L’adresse et la taille de la table de certificats d’attribut. Pour plus d’informations, consultez [la table des certificats d’attribut (image uniquement)](#the-attribute-certificate-table-image-only). <br/> |
| 136/152 <br/> | 8 <br/> | Table de réadressage de base <br/>   | L’adresse et la taille de la table de réadressage de base. Pour plus d’informations, consultez [la section. reloc (image uniquement)](#the-reloc-section-image-only).<br/>                                   |
| 144/160 <br/> | 8 <br/> | Débogage <br/>                   | L’adresse de départ et la taille des données de débogage. Pour plus d’informations, consultez [la section. Debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architecture <br/>            | Réservé, doit avoir la valeur 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | Ptr global <br/>              | RVA de la valeur à stocker dans le registre de pointeur global. Le membre de la taille de cette structure doit avoir la valeur zéro. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Table TLS <br/>               | L’adresse et la taille de la table de stockage local des threads (TLS). Pour plus d’informations, consultez [la section. TLS](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Charger la table de configuration <br/>       | L’adresse et la taille de la table de configuration de charge. Pour plus d’informations, consultez [structure de la configuration de chargement (image uniquement)](#the-load-configuration-structure-image-only).<br/>       |
| 184/200 <br/> | 8 <br/> | Importation liée <br/>            | L’adresse et la taille de la table d’importation liée. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | L’adresse et la taille de la table d’adresses d’importation. Pour plus d’informations, consultez [Importer une table d’adresses](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Retarder le descripteur d’importation <br/> | Adresse et taille du descripteur d’importation à retards. Pour plus d’informations, consultez [tables d’importation à chargement différé (image uniquement)](#delay-load-import-tables-image-only).<br/>                    |
| 208/224 <br/> | 8 <br/> | En-tête CLR Runtime <br/>      | L’adresse et la taille de l’en-tête du runtime CLR. Pour plus d’informations, consultez [la section. cormeta (objet uniquement)](#the-cormeta-section-object-only).<br/>                                |
| 216/232 <br/> | 8 <br/> | Réservé, doit être égal à zéro <br/>  |                                                                                                                                                                                      |

L’entrée de la table de certificats pointe vers une table de certificats d’attribut. Ces certificats ne sont pas chargés en mémoire dans le cadre de l’image. Par conséquent, le premier champ de cette entrée, qui est normalement un RVA, est un pointeur de fichier à la place.

## <a name="section-table-section-headers"></a>Table de section (en-têtes de section)

- [Indicateurs de section](#section-flags)
- [Sections groupées (objet uniquement)](#grouped-sections-object-only)

Chaque ligne de la table de section est en fait un en-tête de section. Ce tableau suit immédiatement l’en-tête facultatif, le cas échéant. Ce positionnement est nécessaire, car l’en-tête de fichier ne contient pas de pointeur direct vers la table de section. Au lieu de cela, l’emplacement de la table de section est déterminé par le calcul de l’emplacement du premier octet après les en-têtes. Veillez à utiliser la taille de l’en-tête facultatif comme spécifié dans l’en-tête du fichier.

Le nombre d’entrées dans la table de section est donné par le champ NumberOfSections dans l’en-tête de fichier. Les entrées de la table de section sont numérotées à partir de un (1). Les entrées de la section du code et de la mémoire de données sont dans l’ordre choisi par l’éditeur de liens.

Dans un fichier image, le SAV pour les sections doit être assigné par l’éditeur de liens pour qu’il soit dans l’ordre croissant et adjacent, et il doit s’agir d’un multiple de la valeur alignement de section dans l’en-tête facultatif.

Chaque en-tête de section (section Table Entry) a le format suivant, pour un total de 40 octets par entrée.



| Offset         | Taille          | Champ                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name <br/>                 | Chaîne encodée en UTF-8 de 8 octets et remplie par null. Si la chaîne contient exactement 8 caractères, il n’y a pas de valeur null de fin. Pour les noms plus longs, ce champ contient une barre oblique (/) qui est suivie d’une représentation ASCII d’un nombre décimal qui est un décalage dans la table de chaînes. Les images exécutables n’utilisent pas de table de chaînes et ne prennent pas en charge les noms de section de plus de 8 caractères. Les noms longs dans les fichiers objets sont tronqués s’ils sont émis dans un fichier exécutable. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Taille totale de la section lorsqu’elle est chargée en mémoire. Si cette valeur est supérieure à SizeOfRawData, la section est remplie de zéro. Ce champ est valide uniquement pour les images exécutables et doit avoir la valeur zéro pour les fichiers objets. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Pour les images exécutables, adresse du premier octet de la section par rapport à la base de l’image lorsque la section est chargée en mémoire. Pour les fichiers objets, ce champ correspond à l’adresse du premier octet avant l’application de la réadressage. par souci de simplicité, les compilateurs doivent définir cette valeur sur zéro. Dans le cas contraire, il s’agit d’une valeur arbitraire qui est soustraite des décalages au cours du déplacement. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | La taille de la section (pour les fichiers objets) ou la taille des données initialisées sur le disque (pour les fichiers image). Pour les images exécutables, il doit s’agir d’un multiple de assigne FileAlignment à partir de l’en-tête facultatif. Si la valeur est inférieure à VirtualSize, le reste de la section est rempli à zéro. Étant donné que le champ SizeOfRawData est arrondi, mais que le champ VirtualSize n’est pas, il est possible que SizeOfRawData soit supérieur à VirtualSize également. Quand une section contient uniquement des données non initialisées, ce champ doit être égal à zéro. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Pointeur de fichier vers la première page de la section dans le fichier COFF. Pour les images exécutables, il doit s’agir d’un multiple de assigne FileAlignment à partir de l’en-tête facultatif. Pour les fichiers objets, la valeur doit être alignée sur une limite de 4 octets pour des performances optimales. Quand une section contient uniquement des données non initialisées, ce champ doit être égal à zéro. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Pointeur de fichier vers le début des entrées de réadressage pour la section. Il a la valeur zéro pour les images exécutables ou s’il n’y a pas de réadressage. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Pointeur de fichier qui pointe vers le début des entrées de numéro de ligne pour la section. Cette valeur est définie sur zéro s’il n’y a pas de numéros de ligne COFF. Cette valeur doit être égale à zéro pour une image, car les informations de débogage COFF sont dépréciées. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | Nombre d’entrées de réadressage pour la section. Cette valeur est définie sur zéro pour les images exécutables. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Nombre d’entrées de numéro de ligne pour la section. Cette valeur doit être égale à zéro pour une image, car les informations de débogage COFF sont dépréciées. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Caractéristiques <br/>      | Indicateurs qui décrivent les caractéristiques de la section. Pour plus d’informations, consultez [indicateurs de section](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Indicateurs de section

Les indicateurs de section dans le champ caractéristiques de l’en-tête de section indiquent les caractéristiques de la section.



| Indicateur                                              | Valeur                  | Description                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ de \_ type SCN \_ sans \_ bloc <br/>             | 0x00000008 <br/> | La section ne doit pas être remplie à la limite suivante. Cet indicateur est obsolète et est remplacé par IMAGE \_ SCN \_ align \_ 1BYTES. Cela est valide uniquement pour les fichiers objets. <br/> |
|                                                   | 0x00000010 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE du code de l’IMAGE \_ SCN \_ CNT \_ <br/>                 | 0x00000020 <br/> | La section contient du code exécutable. <br/>                                                                                                                           |
| IMAGE \_ \_ \_ données initialisées SCN \_ CNT <br/>    | 0x00000040 <br/> | La section contient des données initialisées. <br/>                                                                                                                          |
| IMAGE \_ \_ \_ données non initialisées SCN \_ CNT <br/> | 0x00000080 <br/> | La section contient des données non initialisées. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ autre <br/>                | 0x00000100 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ info <br/>                 | 0x00000200 <br/> | La section contient des commentaires ou d’autres informations. La section. drectve a ce type. Cela n’est valide que pour les fichiers objets. <br/>                                    |
|                                                   | 0x00000400 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ Supprimer <br/>               | 0x00000800 <br/> | La section ne fait pas partie de l’image. Cela est valide uniquement pour les fichiers objets. <br/>                                                                             |
| IMAGE \_ SCN \_ LNK \_ COMDAT <br/>               | 0x00001000 <br/> | La section contient des données COMDAT. Pour plus d’informations, consultez la [section COMDAT sections (Object only)](#comdat-sections-object-only). Cela est valide uniquement pour les fichiers objets. <br/> |
| IMAGE \_ SCN \_ GPREL <br/>                     | 0x00008000 <br/> | La section contient des données référencées par le biais du pointeur global (GP). <br/>                                                                                           |
| IMAGE \_ de \_ mémoire SCN \_ PURGEABLE <br/>            | 0x00020000 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ mém \_ 16 bits <br/>                | 0x00020000 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ du \_ MEM SCN \_ verrouillé <br/>               | 0x00040000 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| préchargement de l’IMAGE \_ SCN \_ MEM \_ <br/>              | 0x00080000 <br/> | Réservé pour un usage futur. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ align \_ 1BYTES <br/>             | 0x00100000 <br/> | Aligner les données sur une limite de 1 octet. Valide uniquement pour les fichiers objets. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 2BYTES <br/>             | 0x00200000 <br/> | Aligner les données sur une limite de 2 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 4BYTES <br/>             | 0x00300000 <br/> | Aligner les données sur une limite de 4 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 8BYTES <br/>             | 0x00400000 <br/> | Aligner les données sur une limite de 8 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 16BYTES <br/>            | 0x00500000 <br/> | Aligner les données sur une limite de 16 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 32BYTES <br/>            | 0x00600000 <br/> | Aligner les données sur une limite de 32 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 64BYTES <br/>            | 0x00700000 <br/> | Aligner les données sur une limite de 64 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 128BYTES <br/>           | 0x00800000 <br/> | Aligner les données sur une limite de 128 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 256BYTES <br/>           | 0x00900000 <br/> | Aligner les données sur une limite de 256 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 512BYTES <br/>           | 0x00A00000 <br/> | Aligner les données sur une limite de 512 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Aligner les données sur une limite de 1024 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Aligner les données sur une limite de 2048 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Aligner les données sur une limite de 4096 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Aligner les données sur une limite de 8192 octets. Valide uniquement pour les fichiers objets. <br/>                                                                                               |
| IMAGE \_ SCN \_ LNK \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | La section contient des réadressages étendus. <br/>                                                                                                                      |
| IMAGE de \_ mémoire SCN qui est \_ \_ Ignorable <br/>          | 0x02000000 <br/> | La section peut être ignorée si nécessaire. <br/>                                                                                                                         |
| IMAGE \_ \_ du MEM SCN \_ non \_ mis en cache <br/>          | 0x04000000 <br/> | La section ne peut pas être mise en cache. <br/>                                                                                                                                   |
| IMAGE \_ \_ mémoire SCN \_ non \_ paginée <br/>           | 0x08000000 <br/> | La section n’est pas paginable. <br/>                                                                                                                                    |
| IMAGE \_ SCN \_ MEM \_ partagé <br/>               | 0x10000000 <br/> | La section peut être partagée en mémoire. <br/>                                                                                                                            |
| IMAGE \_ de \_ mémoire SCN en \_ exécution <br/>              | 0x20000000 <br/> | La section peut être exécutée en tant que code. <br/>                                                                                                                            |
| IMAGE \_ \_ mémoire SCN \_ en lecture <br/>                 | 0x40000000 <br/> | La section peut être lue. <br/>                                                                                                                                        |
| IMAGE \_ mémoire SCN en \_ \_ écriture <br/>                | 0x80000000 <br/> | La section peut être écrite dans. <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ LNK \_ NRELOC \_ OVFL indique que le nombre de réadressages pour la section dépasse les 16 bits qui lui sont réservés dans l’en-tête de la section. Si le bit est défini et que le champ NumberOfRelocations dans l’en-tête de la section est 0xFFFF, le nombre réel de réadressages est stocké dans le champ VirtualAddress de 32 bits du premier réadressage. Il s’agit d’une erreur \_ si \_ l’image SCN LNK \_ NRELOC \_ OVFL est définie et qu’il y a moins de 0xFFFF réadressages dans la section.

### <a name="grouped-sections-object-only"></a>Sections groupées (objet uniquement)

Le « $ » ? le caractère (signe dollar) a une interprétation spéciale dans les noms de section dans les fichiers objets.

Lorsque vous déterminez la section d’image qui contiendra le contenu d’une section d’objet, l’éditeur de liens ignore le « $ » ? et tous les caractères qui le suivent. Ainsi, une section de l’objet nommée. le **texte $ X** contribue en fait à la section **. Text** de l’image.

Toutefois, les caractères qui suivent le caractère « $ » ? Déterminez l’ordre des contributions à la section image. Toutes les contributions ayant le même nom de section d’objet sont allouées de façon contiguë dans l’image, et les blocs de contributions sont triés dans l’ordre lexical par nom de section d’objet. Par conséquent, tout dans les fichiers objets avec le nom de la section **. Text $ X** se termine ensemble, après les contributions **. Text $ W** et avant les contributions **. Text $ Y** .

Le nom de la section dans un fichier image ne contient jamais de « $ » ? .

## <a name="other-contents-of-the-file"></a>Autre contenu du fichier

- [Données de la section](#section-data)
- [Réadressages COFF (objet uniquement)](#coff-relocations-object-only)
  - [Indicateurs de type](#type-indicators)
- [Numéros de ligne COFF (déconseillé)](#coff-line-numbers-deprecated)
- [Table de symboles COFF](#coff-symbol-table)
  - [Représentation du nom de symbole](#symbol-name-representation)
  - [Valeurs des numéros de section](#section-number-values)
  - [Représentation de type](#type-representation)
  - [Stockage Type](#storage-class)
- [Enregistrements de symboles auxiliaires](#auxiliary-symbol-records)
  - [Format auxiliaire 1 : définitions de fonction](#auxiliary-format-1-function-definitions)
  - [Format auxiliaire 2 : symboles. BF et. EF](#auxiliary-format-2-bf-and-ef-symbols)
  - [Format auxiliaire 3 : externes faibles](#auxiliary-format-3-weak-externals)
  - [Format auxiliaire 4 : fichiers](#auxiliary-format-4-files)
  - [Format auxiliaire 5 : définitions de section](#auxiliary-format-5-section-definitions)
  - [Sections COMDAT (objet uniquement)](#comdat-sections-object-only)
  - [Définition du jeton CLR (objet uniquement)](#clr-token-definition-object-only)
- [Table de chaînes COFF](#coff-string-table)
- [Table de certificats d’attribut (image uniquement)](#the-attribute-certificate-table-image-only)
  - [Données du certificat](#certificate-data)
- [Chargement différé des tables d’importation (image uniquement)](#delay-load-import-tables-image-only)
  - [Table Delay-Load Directory](#the-delay-load-directory-table)
  - [Attributs](#attributes)
  - [Nom](#name)
  - [Handle de module](#module-handle)
  - [Différer la table d’adresses d’importation](#delay-import-address-table)
  - [Retarder la table du nom d’importation](#delay-import-name-table)
  - [Table d’adresses d’importation à liaison différée et horodatage](#delay-bound-import-address-table-and-time-stamp)
  - [Différer la table d’adresses d’importation](#delay-unload-import-address-table)

Les structures de données qui ont été décrites jusqu’à présent, jusqu’à et y compris l’en-tête facultatif, sont toutes situées à un décalage fixe par rapport au début du fichier (ou à partir de l’en-tête PE si le fichier est une image qui contient un stub MS-DOS).

Le reste d’un fichier image ou objet COFF contient des blocs de données qui ne sont pas nécessairement à un décalage de fichier spécifique. Au lieu de cela, les emplacements sont définis par des pointeurs dans l’en-tête facultatif ou un en-tête de section.

Une exception concerne les images dont la valeur alignement de section est inférieure à la taille de page de l’architecture (4 K pour Intel x86 et pour MIPS, et 8 K pour Itanium). Pour obtenir une description de alignement de section, consultez l' [en-tête facultatif (image uniquement)](#optional-header-image-only). Dans ce cas, il existe des contraintes sur le décalage de fichier des données de la section, comme décrit dans la section 5,1, « données de la section ». Une autre exception est que le certificat d’attribut et les informations de débogage doivent être placés à la fin d’un fichier image, avec la table de certificats d’attribut qui précède immédiatement la section de débogage, car le chargeur ne les mappe pas en mémoire. Toutefois, la règle relative au certificat d’attribut et aux informations de débogage ne s’applique pas aux fichiers objets.

### <a name="section-data"></a>Données de la section

Les données initialisées pour une section se composent de blocs d’octets simples. Toutefois, pour les sections qui contiennent des zéros, il n’est pas nécessaire d’inclure les données de la section.

Les données de chaque section se trouvent au niveau du décalage de fichier fourni par le champ PointerToRawData dans l’en-tête de la section. La taille de ces données dans le fichier est indiquée par le champ SizeOfRawData. Si SizeOfRawData est inférieur à VirtualSize, le reste est complété avec des zéros.

Dans un fichier image, les données de la section doivent être alignées sur une limite telle que spécifiée par le champ assigne FileAlignment dans l’en-tête facultatif. Les données de section doivent apparaître dans l’ordre des valeurs RVA pour les sections correspondantes (comme les en-têtes de section individuels dans la table de section).

Il existe des restrictions supplémentaires sur les fichiers image si la valeur alignement de section dans l’en-tête facultatif est inférieure à la taille de page de l’architecture. Pour ces fichiers, l’emplacement des données de section dans le fichier doit correspondre à son emplacement en mémoire lorsque l’image est chargée, afin que le décalage physique pour les données de section soit identique à l’adresse RVA.

### <a name="coff-relocations-object-only"></a>Réadressages COFF (objet uniquement)

Les fichiers objets contiennent des réadressages COFF qui spécifient comment les données de la section doivent être modifiées lorsqu’elles sont placées dans le fichier image, puis chargées en mémoire.

Les fichiers image ne contiennent pas de réadressages COFF, car des adresses ont déjà été affectées à tous les symboles référencés dans un espace d’adressage plat. Une image contient des informations de réadressage sous la forme de réadressages de base dans la section. reloc (sauf si l’image a le \_ fichier image \_ des réadressages \_ attribut supprimé). Pour plus d’informations, consultez [la section. reloc (image uniquement)](#the-reloc-section-image-only).

Pour chaque section d’un fichier objet, un tableau d’enregistrements de longueur fixe contient les réadressages COFF de la section. La position et la longueur du tableau sont spécifiées dans l’en-tête de la section. Chaque élément du tableau a le format suivant.



| Offset        | Taille          | Champ                        | Description                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Adresse de l’élément auquel la réadressage est appliquée. Il s’agit du décalage à partir du début de la section, plus la valeur du champ RVA/offset de la section. Consultez la [section table (en-têtes de section)](#section-table-section-headers). Par exemple, si le premier octet de la section a l’adresse 0x10, le troisième octet a une adresse de 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Index de base zéro dans la table de symboles. Ce symbole indique l’adresse à utiliser pour le déplacement. Si le symbole spécifié a une classe de stockage de section, l’adresse du symbole est l’adresse avec la première section du même nom. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Type <br/>             | Valeur qui indique le type de réadressage qui doit être effectué. Les types de réadressage valides dépendent du type d’ordinateur. Consultez [indicateurs de type](#type-indicators). <br/>                                                                                                                                                                                     |



 

Si le symbole référencé par le champ SymbolTableIndex a la section Storage Class IMAGE \_ sym \_ Class \_ , l’adresse du symbole est le début de la section. La section se trouve généralement dans le même fichier, sauf si le fichier objet fait partie d’une archive (bibliothèque). Dans ce cas, la section se trouve dans tout autre fichier objet de l’archive qui a le même nom de membre d’archive que le fichier objet actuel. (La relation avec le nom du membre d’archive est utilisée dans la liaison des tables d’importation, autrement dit, la section. idata.)

#### <a name="type-indicators"></a>Indicateurs de type

Le champ type de l’enregistrement de réadressage indique le type de réadressage à effectuer. Différents types de réadressage sont définis pour chaque type d’ordinateur.

##### <a name="x64-processors"></a>Processeurs x64

Les indicateurs de type de réadressage suivants sont définis pour les processeurs x64 et compatibles.



| Constante                                | Valeur              | Description                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ amd64 \_ absolue <br/> | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                        |
| IMAGE \_ rel \_ amd64 \_ ADDR64 <br/>   | 0x0001 <br/> | VA 64 bits de la cible de réadressage. <br/>                                                                                                           |
| IMAGE \_ rel \_ amd64 \_ ADDR32 <br/>   | 0x0002 <br/> | VA 32 bits de la cible de réadressage. <br/>                                                                                                           |
| IMAGE \_ rel \_ amd64 \_ ADDR32NB <br/> | 0x0003 <br/> | Adresse 32 bits sans une base d’image (RVA). <br/>                                                                                                   |
| IMAGE \_ rel \_ amd64 \_ REL32 <br/>    | 0x0004 <br/> | Adresse relative 32 bits à partir de l’octet qui suit le réadressage. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Adresse 32 bits relative à la distance par octet 1 à partir du réadressage. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Adresse 32 bits relative à la distance par octet 2 du réadressage. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Adresse 32 bits relative à la distance par octet 3 à partir du réadressage. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Adresse 32 bits relative à la distance par octet 4 du déplacement. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Adresse 32 bits relative à la distance en octets 5 par rapport au déplacement. <br/>                                                                               |
| SECTION d’IMAGE \_ rel \_ amd64 \_ <br/>  | 0x000A <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                  |
| IMAGE \_ rel \_ amd64 \_ SECREL <br/>   | 0x000B <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/> |
| IMAGE \_ rel \_ amd64 \_ SECREL7 <br/>  | 0x000C <br/> | Offset non signé 7 bits à partir de la base de la section qui contient la cible. <br/>                                                                    |
| \_ \_ Jeton amd64 de l’image \_ <br/>    | 0x000D <br/> | Jetons CLR. <br/>                                                                                                                                       |
| IMAGE \_ rel \_ amd64 \_ SREL32 <br/>   | 0x000E <br/> | Valeur dépendante de l’étendue signée 32 bits émise dans l’objet. <br/>                                                                                     |
| \_ \_ Paire amd64 d' \_ image <br/>     | 0x000F <br/> | Paire qui doit suivre immédiatement chaque valeur dépendante de l’étendue. <br/>                                                                                   |
| IMAGE \_ rel \_ amd64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Valeur dépendante de la portée signée 32 bits qui est appliquée au moment de la liaison. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Processeurs ARM

Les indicateurs de type de réadressage suivants sont définis pour les processeurs ARM.



| Constante                                | Valeur              | Description                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ ARM \_ absolu <br/>   | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | VA 32 bits de la cible. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ rel \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ rel \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Déplacement relatif de 24 bits vers la cible. <br/>                                                                                                                                                                                                            |
| IMAGE \_ rel \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Référence à un appel de sous-routine. La référence se compose d’instructions 2 16 bits avec des décalages de 11 bits. <br/>                                                                                                                                                 |
| IMAGE \_ rel \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Adresse relative 32 bits à partir de l’octet qui suit le réadressage. <br/>                                                                                                                                                                                        |
| \_ \_ section ARM de l’image \_ <br/>    | 0x000E <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                                                                           |
| IMAGE \_ rel \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                                                                          |
| IMAGE \_ rel \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | VA 32 bits de la cible. Ce déplacement est appliqué à l’aide d’une instruction MOVW pour les 16 bits de poids faible suivis d’un MOVT pour les 16 bits de poids fort. <br/>                                                                                                              |
| IMAGE \_ rel \_ Thumb \_ MOV32 <br/>    | 0x0011 <br/> | VA 32 bits de la cible. Ce déplacement est appliqué à l’aide d’une instruction MOVW pour les 16 bits de poids faible suivis d’un MOVT pour les 16 bits de poids fort. <br/>                                                                                                              |
| IMAGE \_ rel \_ Thumb \_ BRANCH20 <br/> | 0x0012 <br/> | L’instruction est déterminée par le décalage relatif de 21 bits vers la cible alignée sur 2 octets. Le bit le moins significatif du déplacement est toujours égal à zéro et n’est pas stocké. Ce réadressage correspond à une instruction B conditionnelle Thumb-2 32-bit. <br/> |
| Inutilisé <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ Thumb \_ BRANCH24 <br/> | 0x0014 <br/> | L’instruction est déterminée par le décalage relatif de 25 bits vers la cible alignée sur 2 octets. Le bit le moins significatif du déplacement est égal à zéro et n’est pas stocké. Ce réadressage correspond à une instruction Thumb-2 B. <br/>                            |
| IMAGE \_ rel \_ Thumb \_ BLX23 <br/>    | 0x0015 <br/> | L’instruction est déterminée par le décalage relatif de 25 bits vers la cible alignée sur 4 octets. Les 2 bits de poids faible du déplacement sont nuls et ne sont pas stockés. <br/> Ce réadressage correspond à une instruction Thumb-2 BLX. <br/>                      |
| \_ \_ paire ARM d’image rel \_ <br/>       | 0x0016 <br/> | Le déplacement est valide uniquement lorsqu’il suit immédiatement un REFHI ARM \_ ou un \_ REFHI Thumb. Son SymbolTableIndex contient un déplacement et non un index dans la table de symboles. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Processeurs ARM64

Les indicateurs de type de réadressage suivants sont définis pour les processeurs ARM64.



| Constante                                       | Valeur              | Description                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ ARM64 \_ absolu <br/>        | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                        |
| IMAGE \_ rel \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | VA 32 bits de la cible. <br/>                                                                                                                      |
| IMAGE \_ rel \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                     |
| IMAGE \_ rel \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Déplacement relatif de 26 bits vers la cible, pour les instructions B et BL. <br/>                                                                        |
| IMAGE \_ rel \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | Base de page de la cible, pour l’instruction ADRP. <br/>                                                                                                |
| IMAGE \_ rel \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Déplacement relatif de 12 bits vers la cible, pour l’instruction ADR <br/>                                                                               |
| IMAGE \_ rel \_ ARM64 \_ PAGEOFFSET \_ 12a <br/> | 0x0006 <br/> | Décalage de page sur 12 bits de la cible, pour les instructions ADD/ADDS (immediate) avec un décalage de zéro. <br/>                                                      |
| IMAGE \_ rel \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Décalage de page sur 12 bits de la cible, pour l’instruction LDR (indexée, unsigned immediate). <br/>                                                          |
| IMAGE \_ rel \_ ARM64 \_ SECREL <br/>          | 0x0008 <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/> |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 du décalage de section de la cible, pour obtenir des instructions ADD/ADDS (immediate) avec un décalage de zéro. <br/>                                                  |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 du décalage de section de la cible, pour obtenir des instructions ADD/ADDS (immediate) avec un décalage de zéro. <br/>                                                 |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 du décalage de section de la cible, pour l’instruction LDR (indexée, unsigned immediate). <br/>                                                      |
| \_ \_ Jeton ARM64 d’image rel \_ <br/>           | 0x000C <br/> | Jeton CLR. <br/>                                                                                                                                        |
| IMAGE \_ rel \_ ARM64 \_ section <br/>         | 0x000D <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                  |
| IMAGE \_ rel \_ ARM64 \_ ADDR64 <br/>          | 0x000E <br/> | VA 64 bits de la cible de réadressage. <br/>                                                                                                           |
| IMAGE \_ rel \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Décalage de 19 bits vers la cible de réadressage, pour l’instruction B conditionnelle. <br/>                                                                        |
| IMAGE \_ rel \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Décalage de 14 bits vers la cible de réadressage, pour les instructions TBZ et TBNZ. <br/>                                                                        |
| IMAGE \_ rel \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Adresse relative 32 bits à partir de l’octet qui suit le réadressage. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Processeurs Hitachi SuperH

Les indicateurs de type de réadressage suivants sont définis pour les processeurs SH3 et SH4. Les réadressages spécifiques à SH5 sont notés en tant que fichier SHM (SH Media).



| Constante                                      | Valeur              | Description                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ SH3 \_ absolu <br/>         | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                     |
| \_DIRECT16 rel \_ de l’image \_ <br/>         | 0x0001 <br/> | Référence à l’emplacement 16 bits qui contient le VA du symbole cible. <br/>                                                                                                                                  |
| \_DIRECT32 rel \_ de l’image \_ <br/>         | 0x0002 <br/> | VA 32 bits du symbole cible. <br/>                                                                                                                                                                            |
| \_Direct8 rel \_ de l’image \_ <br/>          | 0x0003 <br/> | Référence à l’emplacement 8 bits qui contient le VA du symbole cible. <br/>                                                                                                                                   |
| IMAGE \_ rel \_ \_ direct8 \_ mot <br/>    | 0x0004 <br/> | Référence à l’instruction 8 bits qui contient le VA de 16 bits effectif du symbole cible. <br/>                                                                                                               |
| \_Direct8 rel \_ \_ de l' \_ image <br/>    | 0x0005 <br/> | Référence à l’instruction 8 bits qui contient le VA 32 bits effectif du symbole cible. <br/>                                                                                                               |
| \_DIRECT4 rel \_ de l’image \_ <br/>          | 0x0006 <br/> | Référence à l’emplacement 8 bits dont les 4 bits de poids faible contiennent le VA du symbole cible. <br/>                                                                                                                        |
| IMAGE \_ rel \_ \_ DIRECT4 \_ mot <br/>    | 0x0007 <br/> | Référence à l’instruction 8 bits dont les 4 bits de poids faible contiennent le VA de 16 bits effectif du symbole cible. <br/>                                                                                                    |
| \_DIRECT4 rel \_ \_ de l' \_ image <br/>    | 0x0008 <br/> | Référence à l’instruction 8 bits dont les 4 bits de poids faible contiennent le VA 32 bits effectif du symbole cible. <br/>                                                                                                    |
| IMAGE \_ rel \_ \_ PCREL8 \_ mot <br/>     | 0x0009 <br/> | Référence à l’instruction 8 bits qui contient l’offset relatif de 16 bits effectif du symbole cible. <br/>                                                                                                  |
| \_PCREL8 rel \_ \_ de l' \_ image <br/>     | 0x000A <br/> | Référence à l’instruction 8 bits qui contient le décalage relatif 32 bits effectif du symbole cible. <br/>                                                                                                  |
| IMAGE \_ rel \_ \_ PCREL12 \_ mot <br/>    | 0x000B <br/> | Référence à l’instruction 16 bits dont les 12 bits de poids faible contiennent le décalage relatif de 16 bits effectif du symbole cible. <br/>                                                                                     |
| IMAGE \_ rel \_ SH3 \_ STARTOF \_ section <br/> | 0x000C <br/> | Référence à un emplacement 32 bits qui est le VA de la section qui contient le symbole cible. <br/>                                                                                                                |
| SECTION d’IMAGE de la \_ \_ \_ \_ section sizeof de la rel. <br/>  | 0x000D <br/> | Référence à l’emplacement 32 bits qui est la taille de la section qui contient le symbole cible. <br/>                                                                                                            |
| SECTION d’IMAGE \_ rel \_ SH3 \_ <br/>          | 0x000E <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                               |
| \_SECREL rel \_ de l’image \_ <br/>           | 0x000F <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                              |
| DIRECT32 de l’IMAGE \_ rel, \_ \_ \_ NB <br/>     | 0x0010 <br/> | RVA 32 bits du symbole cible. <br/>                                                                                                                                                                           |
| \_GPREL4 rel \_ \_ de l' \_ image <br/>     | 0x0011 <br/> | GP relative. <br/>                                                                                                                                                                                                   |
| \_ \_ Jeton SH3 d’image rel \_ <br/>            | 0x0012 <br/> | Jeton CLR. <br/>                                                                                                                                                                                                     |
| IMAGE \_ rel \_ fichier SHM \_ PCRELPT <br/>          | 0x0013 <br/> | Offset de l’instruction actuelle dans longwords. Si le bit nomode n’est pas défini, insérez l’inverse du bit le plus faible au bit 32 pour sélectionner PTA ou PTB. <br/>                                                          |
| IMAGE \_ rel \_ fichier SHM \_ REFLO <br/>            | 0x0014 <br/> | Les 16 bits de poids faible de l’adresse 32 bits. <br/>                                                                                                                                                                         |
| IMAGE \_ rel \_ fichier SHM \_ REFHALF <br/>          | 0x0015 <br/> | Les 16 bits de poids fort de l’adresse 32 bits. <br/>                                                                                                                                                                        |
| IMAGE \_ rel \_ fichier SHM \_ RELLO <br/>            | 0x0016 <br/> | Les 16 bits de poids faible de l’adresse relative. <br/>                                                                                                                                                                       |
| IMAGE \_ rel \_ fichier SHM \_ RELHALF <br/>          | 0x0017 <br/> | Les 16 bits de poids fort de l’adresse relative. <br/>                                                                                                                                                                      |
| \_ \_ paire fichier SHM d' \_ image <br/>             | 0x0018 <br/> | Le déplacement est valide uniquement lorsqu’il suit immédiatement un déplacement REFHALF, RELHALF ou RELLO. Le champ SymbolTableIndex de la réadressage contient un déplacement et non un index dans la table de symboles. <br/> |
| IMAGE \_ rel \_ fichier SHM \_ nomode <br/>           | 0x8000 <br/> | Le réadressage ignore le mode de section. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>processeurs PowerPC IBM

les indicateurs de type de réadressage suivants sont définis pour les processeurs PowerPC.



| Constante                              | Valeur              | Description                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ PPC \_ absolu <br/> | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ rel \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | VA 64 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ rel \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | VA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ rel \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | Les 24 bits de poids faible du VA de la cible. Cela est valide uniquement lorsque le symbole cible est absolu et peut être étendu à sa valeur d’origine. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | Les 16 bits de poids faible du VA de la cible. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | 14 bits de poids faible du VA de la cible. Cela est valide uniquement lorsque le symbole cible est absolu et peut être étendu à sa valeur d’origine. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ rel \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Décalage relatif au PC 24 bits par rapport à l’emplacement du symbole. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Décalage relatif au PC 14 bits par rapport à l’emplacement du symbole. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | RVA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                                                                                                                                                                                       |
| \_section image rel \_ PPC \_ <br/>  | 0x000C <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Décalage de 16 bits de la cible à partir du début de la section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ rel \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | Les 16 bits de poids fort de la VA 32 bits de la cible. Elle est utilisée pour la première instruction dans une séquence à deux instructions qui charge une adresse complète. Ce réadressage doit être immédiatement suivi d’un réadressage de paire dont SymbolTableIndex contient un déplacement 16 bits signé qui est ajouté aux 16 bits supérieurs qui ont été extraits de l’emplacement en cours de déplacement. <br/> |
| IMAGE \_ rel \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | Les 16 bits de poids faible du VA de la cible. <br/>                                                                                                                                                                                                                                                                                                                                     |
| paire d’images \_ rel \_ PPC \_ <br/>     | 0x0012 <br/> | Un déplacement qui est valide uniquement lorsqu’il suit immédiatement un déplacement REFHI ou SECRELHI. Son SymbolTableIndex contient un déplacement et non un index dans la table de symboles. <br/>                                                                                                                                                                                        |
| IMAGE \_ rel \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | Les 16 bits de poids faible du décalage 32 bits de la cible à partir du début de la section. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Déplacement signé 16 bits de la cible par rapport au registre de la stratégie de protection des comptes. <br/>                                                                                                                                                                                                                                                                                               |
| jeton d’IMAGE \_ rel \_ PPC \_ <br/>    | 0x0016 <br/> | Jeton CLR. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Processeurs Intel 386

Les indicateurs de type de réadressage suivants sont définis pour Intel 386 et les processeurs compatibles.



| Constante                               | Valeur              | Description                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ i386 \_ absolu <br/> | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                        |
| IMAGE \_ rel \_ i386 \_ DIR16 <br/>    | 0x0001 <br/> | Non pris en charge. <br/>                                                                                                                                    |
| IMAGE \_ rel \_ i386 \_ REL16 <br/>    | 0x0002 <br/> | Non pris en charge. <br/>                                                                                                                                    |
| IMAGE \_ rel \_ i386 \_ DIR32 <br/>    | 0x0006 <br/> | VA 32 bits de la cible. <br/>                                                                                                                           |
| IMAGE \_ rel \_ i386 \_ DIR32NB <br/>  | 0x0007 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                          |
| IMAGE \_ rel \_ i386 \_ SEG12 <br/>    | 0x0009 <br/> | Non pris en charge. <br/>                                                                                                                                    |
| SECTION d’IMAGE \_ rel \_ i386 \_ <br/>  | 0x000A <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                  |
| IMAGE \_ rel \_ i386 \_ SECREL <br/>   | 0x000B <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/> |
| \_ \_ Jeton i386 d’image rel \_ <br/>    | 0x000C <br/> | Jeton CLR. <br/>                                                                                                                                    |
| IMAGE \_ rel \_ i386 \_ SECREL7 <br/>  | 0x000D <br/> | Décalage de 7 bits par rapport à la base de la section qui contient la cible. <br/>                                                                             |
| IMAGE \_ rel \_ i386 \_ REL32 <br/>    | 0x0014 <br/> | Décalage relatif 32 bits vers la cible. Cela prend en charge la branche relative x86 et les instructions d’appel. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Intel Itanium Processor Family (IPF)

Les indicateurs de type de réadressage suivants sont définis pour la famille de processeurs Intel Itanium et les processeurs compatibles. Notez que les réadressages sur les instructions utilisent le décalage et le numéro d’emplacement du bundle pour le décalage de réadressage.



| Constante                                 | Valeur              | Description                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ ia64 \_ absolu <br/>   | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ ia64 \_ IMM14 <br/>      | 0x0001 <br/> | Le réadressage des instructions peut être suivi d’un réadressage ADDEND dont la valeur est ajoutée à l’adresse cible avant d’être insérée dans l’emplacement spécifié dans le bundle IMM14. La cible de réadressage doit être absolue ou l’image doit être fixe. <br/>                                                                                 |
| IMAGE \_ rel \_ ia64 \_ IMM22 <br/>      | 0x0002 <br/> | Le réadressage des instructions peut être suivi d’un réadressage ADDEND dont la valeur est ajoutée à l’adresse cible avant d’être insérée dans l’emplacement spécifié dans le bundle IMM22. La cible de réadressage doit être absolue ou l’image doit être fixe. <br/>                                                                                 |
| IMAGE \_ rel \_ ia64 \_ IMM64 <br/>      | 0x0003 <br/> | Le numéro d’emplacement de ce réadressage doit être un (1). Le réadressage peut être suivi d’un réadressage ADDEND dont la valeur est ajoutée à l’adresse cible avant d’être stockée dans les trois emplacements du bundle IMM64. <br/>                                                                                                                   |
| IMAGE \_ rel \_ ia64 \_ DIR32 <br/>      | 0x0004 <br/> | VA 32 bits de la cible. Cela est pris en charge uniquement pour/LARGEADDRESSAWARE : aucune image. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ rel \_ ia64 \_ DIR64 <br/>      | 0x0005 <br/> | VA 64 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ rel \_ ia64 \_ PCREL21B <br/>   | 0x0006 <br/> | L’instruction est déterminée par le décalage relatif de 25 bits vers la cible alignée sur 16 bits. Les 4 bits de poids faible du déplacement sont nuls et ne sont pas stockés. <br/>                                                                                                                                                                     |
| IMAGE \_ rel \_ ia64 \_ PCREL21M <br/>   | 0x0007 <br/> | L’instruction est déterminée par le décalage relatif de 25 bits vers la cible alignée sur 16 bits. Les 4 bits de poids faible du déplacement, qui sont nuls, ne sont pas stockés. <br/>                                                                                                                                                                 |
| IMAGE \_ rel \_ ia64 \_ PCREL21F <br/>   | 0x0008 <br/> | Le LSBs du décalage de ce déplacement doit contenir le numéro d’emplacement, tandis que le reste est l’adresse du bundle. Le bundle est résolu avec le déplacement relatif de 25 bits vers la cible alignée sur 16 bits. Les 4 bits de poids faible du déplacement sont nuls et ne sont pas stockés. <br/>                                                                |
| IMAGE \_ rel \_ ia64 \_ GPREL22 <br/>    | 0x0009 <br/> | Le réadressage des instructions peut être suivi d’un réadressage ADDEND dont la valeur est ajoutée à l’adresse cible, puis d’un décalage relatif à la stratégie de groupe (GP) de 22 bits qui est calculé et appliqué au Bundle GPREL22. <br/>                                                                                                                            |
| IMAGE \_ rel \_ ia64 \_ LTOFF22 <br/>    | 0x000A <br/> | L’instruction est redéfinie avec l’offset relatif à la stratégie de délimiteur de l’élément de configuration de la stratégie de niveau « 22 bits » à l’entrée de table littérale L’éditeur de liens crée cette entrée de table littérale en fonction de ce déplacement et du réadressage de ADDEND qui peuvent suivre. <br/>                                                                                                        |
| SECTION d’IMAGE \_ rel \_ ia64 \_ <br/>    | 0x000B <br/> | L’index de la section 16 bits de la section contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                                                                                                                                                         |
| IMAGE \_ rel \_ ia64 \_ SECREL22 <br/>   | 0x000C <br/> | L’instruction est redéfinie avec l’offset de 22 bits de la cible à partir du début de la section. Ce réadressage peut être immédiatement suivi d’un déplacement ADDEND, dont le champ de valeur contient le décalage non signé 32 bits de la cible à partir du début de la section. <br/>                                                     |
| IMAGE \_ rel \_ ia64 \_ SECREL64I <br/>  | 0x000D <br/> | Le numéro d’emplacement de ce réadressage doit être un (1). L’instruction est redéfinie avec l’offset de 64 bits de la cible à partir du début de sa section. Ce réadressage peut être immédiatement suivi par un réadressage ADDEND dont le champ de valeur contient le décalage non signé 32 bits de la cible à partir du début de la section. <br/> |
| IMAGE \_ rel \_ ia64 \_ SECREL32 <br/>   | 0x000E <br/> | Adresse des données à replacer avec le décalage 32 bits de la cible à partir du début de la section. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ ia64 \_ DIR32NB <br/>    | 0x0010 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ rel \_ ia64 \_ SREL14 <br/>     | 0x0011 <br/> | Cela s’applique à un immédian 14 bits signé qui contient la différence entre deux cibles réadressables. Il s’agit d’un champ déclaratif pour l’éditeur de liens qui indique que le compilateur a déjà émis cette valeur. <br/>                                                                                                              |
| IMAGE \_ rel \_ ia64 \_ SREL22 <br/>     | 0x0012 <br/> | Cela s’applique à un immédian 22 bits signé qui contient la différence entre deux cibles réadressables. Il s’agit d’un champ déclaratif pour l’éditeur de liens qui indique que le compilateur a déjà émis cette valeur. <br/>                                                                                                              |
| IMAGE \_ rel \_ ia64 \_ SREL32 <br/>     | 0x0013 <br/> | Cela s’applique à un immédian 32 bits signé qui contient la différence entre deux valeurs réadressables. Il s’agit d’un champ déclaratif pour l’éditeur de liens qui indique que le compilateur a déjà émis cette valeur. <br/>                                                                                                               |
| IMAGE \_ rel \_ ia64 \_ UREL32 <br/>     | 0x0014 <br/> | Cela s’applique à un instantané non signé 32 bits qui contient la différence entre deux valeurs réadressables. Il s’agit d’un champ déclaratif pour l’éditeur de liens qui indique que le compilateur a déjà émis cette valeur. <br/>                                                                                                            |
| IMAGE \_ rel \_ ia64 \_ PCREL60X <br/>   | 0x0015 <br/> | Correction relative à un PC 60 bits qui reste toujours comme une instruction BRL d’un bundle MLX. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ ia64 \_ PCREL60B <br/>   | 0x0016 <br/> | Correction relative à un PC 60 bits. Si le déplacement cible s’ajuste à un champ de 25 bits signé, convertissez le lot entier en un bundle MBB avec NOP. B dans l’emplacement 1 et une instruction BR de 25 bits (avec les 4 bits les plus bas tous nuls et supprimés) dans l’emplacement 2. <br/>                                                                                          |
| IMAGE \_ rel \_ ia64 \_ PCREL60F <br/>   | 0x0017 <br/> | Correction relative à un PC 60 bits. Si le déplacement cible s’ajuste à un champ de 25 bits signé, convertissez le lot entier en un bundle MFB avec NOP. F dans l’emplacement 1 et une instruction 25 bits (4 bits les plus faibles, toutes zéro et supprimée) BR dans l’emplacement 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ ia64 \_ PCREL60I <br/>   | 0x0018 <br/> | Correction relative à un PC 60 bits. Si le déplacement cible s’ajuste à un champ de 25 bits signé, convertissez le lot entier en un bundle MIB avec NOP. I dans l’emplacement 1 et une instruction 25 bits (4 bits les plus faibles, toutes zéro et supprimée) BR dans l’emplacement 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ ia64 \_ PCREL60M <br/>   | 0x0019 <br/> | Correction relative à un PC 60 bits. Si le déplacement cible s’ajuste à un champ de 25 bits signé, convertissez le lot entier en bundle avec NOP. M dans l’emplacement 1 et une instruction 25 bits (4 bits les plus faibles, toutes zéro et supprimée) BR dans l’emplacement 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ ia64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Correction relative à GP 64 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| \_ \_ Jeton ia64 d’image rel \_ <br/>      | 0x001b <br/> | Jeton CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ ia64 \_ GPREL32 <br/>    | 0x011B <br/> | Correction relative à GP 32 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ rel \_ ia64 \_ ADDEND <br/>     | 0x001F <br/> | Le déplacement est valide uniquement lorsqu’il suit immédiatement l’un des réadressages suivants : IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I ou SECREL32. Sa valeur contient le addend à appliquer aux instructions dans un bundle, et non aux données. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Processeurs MIPS

Les indicateurs de type de réadressage suivants sont définis pour les processeurs MIPS.



| Constante                                | Valeur              | Description                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ de \_ mips \_ rel <br/>  | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                                                                                                                                                                              |
| \_REFHALF rel \_ mips de l’image \_ <br/>   | 0x0001 <br/> | Les 16 bits de poids fort de la VA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                             |
| \_REFWORD rel \_ mips de l’image \_ <br/>   | 0x0002 <br/> | VA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| \_JMPADDR rel \_ mips de l’image \_ <br/>   | 0x0003 <br/> | 26 bits de poids faible du VA de la cible. Cela prend en charge les instructions MIPS J et JAL. <br/>                                                                                                                                                                                                                                                                                      |
| \_REFHI rel \_ mips de l’image \_ <br/>     | 0x0004 <br/> | Les 16 bits de poids fort de la VA 32 bits de la cible. Elle est utilisée pour la première instruction dans une séquence à deux instructions qui charge une adresse complète. Ce réadressage doit être immédiatement suivi d’un réadressage de paire dont SymbolTableIndex contient un déplacement 16 bits signé qui est ajouté aux 16 bits supérieurs qui sont tirés de l’emplacement en cours de déplacement. <br/> |
| \_REFLO rel \_ mips de l’image \_ <br/>     | 0x0005 <br/> | Les 16 bits de poids faible du VA de la cible. <br/>                                                                                                                                                                                                                                                                                                                                     |
| \_GPREL rel \_ mips de l’image \_ <br/>     | 0x0006 <br/> | Déplacement signé 16 bits de la cible par rapport au registre de la stratégie de protection des comptes. <br/>                                                                                                                                                                                                                                                                                                 |
| \_ \_ littéral mips d’image rel \_ <br/>   | 0x0007 <br/> | Identique à la GPREL des mips d’IMAGE \_ rel \_ \_ . <br/>                                                                                                                                                                                                                                                                                                                                    |
| SECTION d’IMAGE \_ rel \_ mips \_ <br/>   | 0x000A <br/> | L’index de la section 16 bits de la section contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                                                                                                                                                                                             |
| \_SECREL rel \_ mips de l’image \_ <br/>    | 0x000B <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                                                                                                                                                                                       |
| \_SECRELLO rel \_ mips de l’image \_ <br/>  | 0x000C <br/> | Les 16 bits de poids faible du décalage 32 bits de la cible à partir du début de la section. <br/>                                                                                                                                                                                                                                                                                   |
| \_SECRELHI rel \_ mips de l’image \_ <br/>  | 0x000D <br/> | Les 16 bits de poids fort de l’offset 32 bits de la cible à partir du début de la section. Un \_ \_ réadressage de paire mips d’image rel \_ doit immédiatement suivre celui-ci. Le SymbolTableIndex du réadressage de paire contient un déplacement 16 bits signé qui est ajouté aux 16 bits supérieurs qui sont extraits de l’emplacement en cours de déplacement. <br/>                            |
| \_JMPADDR16 rel \_ mips de l’image \_ <br/> | 0x0010 <br/> | 26 bits de poids faible du VA de la cible. Cela prend en charge l’instruction MIPS16 JAL. <br/>                                                                                                                                                                                                                                                                                           |
| \_REFWORDNB rel \_ mips de l’image \_ <br/> | 0x0022 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ paire mips d’image rel \_ <br/>      | 0x0025 <br/> | Le déplacement est valide uniquement lorsqu’il suit immédiatement un déplacement REFHI ou SECRELHI. Son SymbolTableIndex contient un déplacement et non un index dans la table de symboles. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Mitsubishi M32R

Les indicateurs de type de réadressage suivants sont définis pour les processeurs M32R Mitsubishi.



| Constante                               | Valeur              | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ m32r \_ absolu <br/> | 0x0000 <br/> | Le déplacement est ignoré. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ m32r \_ ADDR32 <br/>   | 0x0001 <br/> | VA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ m32r \_ ADDR32NB <br/> | 0x0002 <br/> | RVA 32 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ m32r \_ ADDR24 <br/>   | 0x0003 <br/> | VA de 24 bits de la cible. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ m32r \_ GPREL16 <br/>  | 0x0004 <br/> | Offset 16 bits de la cible à partir du registre de la stratégie de protection des stratégies. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ m32r \_ PCREL24 <br/>  | 0x0005 <br/> | Décalage de 24 bits de la cible par rapport au compteur de programme (PC), décalé vers la gauche de 2 bits et signe étendu <br/>                                                                                                                                                                                                                                                                                                |
| IMAGE \_ rel \_ m32r \_ PCREL16 <br/>  | 0x0006 <br/> | Décalage de 16 bits de la cible par rapport au PC, décalé de la gauche de 2 bits et du signe étendu <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ m32r \_ PCREL8 <br/>   | 0x0007 <br/> | Décalage 8 bits de la cible par rapport au PC, décalé de la gauche de 2 bits et du signe étendu <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ m32r \_ REFHALF <br/>  | 0x0008 <br/> | 16 MSBs du VA cible. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ m32r \_ REFHI <br/>    | 0x0009 <br/> | 16 MSBs du VA cible, ajusté pour l’extension de signe LSB. Elle est utilisée pour la première instruction dans une séquence à deux instructions qui charge une adresse 32 bits complète. Ce réadressage doit être immédiatement suivi d’un réadressage de paire dont SymbolTableIndex contient un déplacement 16 bits signé qui est ajouté aux 16 bits supérieurs qui sont tirés de l’emplacement en cours de déplacement. <br/> |
| IMAGE \_ rel \_ m32r \_ REFLO <br/>    | 0x000A <br/> | 16 LSBs du VA cible. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| \_ \_ Paire m32r d' \_ image <br/>     | 0x000B <br/> | Le réadressage doit suivre le réadressage REFHI. Son SymbolTableIndex contient un déplacement et non un index dans la table de symboles. <br/>                                                                                                                                                                                                                                                             |
| IMAGE \_ rel \_ m32r \_ section <br/>  | 0x000C <br/> | Index de la section 16 bits de la section qui contient la cible. Utilisé pour prendre en charge les informations de débogage. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ m32r \_ SECREL <br/>   | 0x000D <br/> | Offset 32 bits de la cible à partir du début de sa section. Cela permet de prendre en charge les informations de débogage et le stockage local des threads statiques. <br/>                                                                                                                                                                                                                                                 |
| \_ \_ Jeton m32r d’image rel \_ <br/>    | 0x000E <br/> | Jeton CLR. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Numéros de ligne COFF (déconseillé)

Les numéros de ligne COFF ne sont plus produits et, à l’avenir, ne sont pas consommés.

Les numéros de ligne COFF indiquent la relation entre le code et les numéros de ligne dans les fichiers sources. Le format Microsoft pour les numéros de ligne COFF est semblable au format COFF standard, mais il a été étendu pour permettre à une section unique d’être liée à des numéros de ligne dans plusieurs fichiers sources.

Les numéros de ligne COFF se composent d’un tableau d’enregistrements de longueur fixe. L’emplacement (décalage de fichier) et la taille du tableau sont spécifiés dans l’en-tête de la section. Chaque enregistrement de numéro de ligne est au format suivant.



| Offset        | Taille          | Champ                  | Description                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Type ( \* ) <br/>  | Il s’agit d’une Union de deux champs : SymbolTableIndex et VirtualAddress. L’utilisation de SymbolTableIndex ou d’un RVA dépend de la valeur de LineNumber. <br/> |
| 4 <br/> | 2 <br/> | LineNumber <br/> | Si la valeur est différente de zéro, ce champ spécifie un numéro de ligne de base 1. Lorsque la valeur est égale à zéro, le champ de type est interprété comme un index de table de symboles pour une fonction. <br/>    |



 

Le champ de type est une Union de champs de 2 4 octets : SymbolTableIndex et VirtualAddress.



| Offset        | Taille          | Champ                        | Description                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Utilisé lorsque LineNumber est égal à zéro : index de l’entrée de table de symboles pour une fonction. Ce format est utilisé pour indiquer la fonction à laquelle un groupe d’enregistrements de numéro de ligne fait référence. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Utilisé lorsque LineNumber est différent de zéro : l’adresse RVA du code exécutable qui correspond à la ligne source indiquée. Dans un fichier objet, contient le VA dans la section. <br/> |



 

Un enregistrement de numéro de ligne peut affecter la valeur zéro au champ LineNumber et pointer vers une définition de fonction dans la table de symboles, ou il peut fonctionner comme une entrée de numéro de ligne standard en donnant un entier positif (numéro de ligne) et l’adresse correspondante dans le code de l’objet.

Un groupe d’entrées de numéro de ligne commence toujours par le premier format : l’index d’un symbole de fonction. S’il s’agit du premier enregistrement de numéro de ligne dans la section, il s’agit également du nom de symbole COMDAT pour la fonction si l’indicateur COMDAT de la section est défini. Consultez les [sections COMDAT (objet uniquement)](#comdat-sections-object-only). L’enregistrement auxiliaire de la fonction dans la table de symboles a un pointeur vers le champ LineNumber qui pointe vers ce même enregistrement de numéro de ligne.

Un enregistrement qui identifie une fonction est suivi d’un nombre quelconque d’entrées de numéro de ligne qui fournissent des informations de numéro de ligne réelles (c’est-à-dire des entrées avec LineNumber supérieur à zéro). Ces entrées sont de base un, par rapport au début de la fonction, et représentent chaque ligne source dans la fonction à l’exception de la première ligne.

Par exemple, le premier enregistrement de numéro de ligne de l’exemple suivant spécifie la fonction ReverseSign (SymbolTableIndex de ReverseSign et LineNumber ayant la valeur zéro). Ensuite, les enregistrements avec les valeurs LineNumber 1, 2 et 3 se suivent, correspondant aux lignes sources, comme indiqué ci-dessous :


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Table de symboles COFF

La table de symboles de cette section est héritée du format COFF traditionnel. il est différent de Microsoft Visual C++ informations de débogage. Un fichier peut contenir à la fois une table de symboles COFF et Visual C++ informations de débogage, et les deux sont conservés séparément. Certains outils Microsoft utilisent la table de symboles à des fins limitées mais importantes, telles que la communication des informations COMDAT à l’éditeur de liens. Les noms de section et les noms de fichiers, ainsi que les symboles de code et de données, sont répertoriés dans la table de symboles.

L’emplacement de la table de symboles est indiqué dans l’en-tête COFF.

La table de symboles est un tableau d’enregistrements, dont la longueur est de 18 octets. Chaque enregistrement est un enregistrement de table de symboles standard ou auxiliaire. Un enregistrement standard définit un symbole ou un nom et a le format suivant.



| Offset         | Taille          | Champ                          | Description                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name ( \* ) <br/>          | Nom du symbole, représenté par une Union de trois structures. Un tableau de 8 octets est utilisé si le nom ne dépasse pas 8 octets. Pour plus d’informations, consultez [représentation du nom de symbole](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Valeur <br/>              | Valeur associée au symbole. L’interprétation de ce champ dépend de SectionNumber et de StorageClass. Une signification type est l’adresse réadressable. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Entier signé qui identifie la section, à l’aide d’un index de base un dans la table de section. Certaines valeurs ont une signification particulière, telle que définie dans la section 5.4.2, « valeurs des numéros de section ». <br/>                                         |
| 14 <br/> | 2 <br/> | Type <br/>               | Nombre qui représente le type. Les outils Microsoft définissent ce champ sur 0x20 (Function) ou 0x0 (pas une fonction). Pour plus d’informations, consultez [représentation de type](#type-representation). <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Valeur énumérée qui représente la classe de stockage. pour plus d’informations, consultez [Stockage classe](#storage-class). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | Nombre d’entrées de table de symboles auxiliaires qui suivent cet enregistrement. <br/>                                                                                                                                                           |



 

Zéro, un ou plusieurs enregistrements de table de symboles auxiliaires suivent immédiatement chaque enregistrement de table de symboles standard. Toutefois, en général, il n’est pas plus d’un enregistrement de table de symboles auxiliaire qui suit un enregistrement de table de symboles standard (à l’exception des enregistrements. file avec des noms de fichiers longs). Chaque enregistrement auxiliaire est de la même taille qu’un enregistrement de table de symboles standard (18 octets), mais au lieu de définir un nouveau symbole, l’enregistrement auxiliaire fournit des informations supplémentaires sur le dernier symbole défini. Le choix des formats à utiliser dépend du champ StorageClass. Les formats actuellement définis pour les enregistrements de table de symboles auxiliaires sont indiqués dans la section 5,5, « enregistrements de symboles auxiliaires ».

Les outils qui lisent les tables de symboles COFF doivent ignorer les enregistrements de symboles auxiliaires dont l’interprétation est inconnue. Cela permet d’étendre le format de table de symboles pour ajouter de nouveaux enregistrements auxiliaires, sans arrêter les outils existants.

#### <a name="symbol-name-representation"></a>Représentation du nom de symbole

Le champ ShortName dans une table de symboles se compose de 8 octets qui contiennent le nom lui-même, s’il n’est pas supérieur à 8 octets, ou si le champ ShortName donne un décalage dans la table de chaînes. Pour déterminer si le nom lui-même ou un décalage est donné, testez les 4 premiers octets pour obtenir une égalité égale à zéro.

Par Convention, les noms sont traités comme des chaînes encodées en UTF-8 se terminant par zéro.



| Offset        | Taille          | Champ                 | Description                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | NomCourt <br/> | Tableau de 8 octets. Ce tableau est complété avec des valeurs NULL à droite si le nom comporte moins de 8 octets. <br/> |
| 0 <br/> | 4 <br/> | Zéros <br/>    | Champ défini sur tous les zéros si le nom comporte plus de 8 octets. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Offset dans la table de chaînes. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valeurs des numéros de section

Normalement, le champ de valeur de section dans une entrée de table de symboles est un index de base un dans la table de section. Toutefois, ce champ est un entier signé et peut prendre des valeurs négatives. Les valeurs suivantes, inférieures à un, ont des significations particulières.



| Constante                          | Valeur          | Description                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sym image \_ non défini <br/> | 0 <br/>  | Une section n’est pas encore affectée à l’enregistrement de symboles. La valeur zéro indique qu’une référence à un symbole externe est définie ailleurs. Une valeur différente de zéro est un symbole commun avec une taille spécifiée par la valeur. <br/> |
| IMAGE \_ sym \_ absolue <br/>  | -1 <br/> | Le symbole a une valeur absolue (non réadressable) et n’est pas une adresse. <br/>                                                                                                                                                  |
| IMAGE \_ de \_ débogage de sym <br/>     | -2 <br/> | Le symbole fournit des informations générales sur le type ou le débogage, mais ne correspond pas à une section. Les outils Microsoft utilisent ce paramètre avec les enregistrements. file (fichier de classe de stockage). <br/>                                            |



 

#### <a name="type-representation"></a>Représentation de type

Le champ de type d’une entrée de table de symboles contient 2 octets, où chaque octet représente des informations de type. LSB représente le type de données simple (base) et l’MSB représente le type complexe, le cas échéant :



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Type complexe : aucun, pointeur, fonction, tableau. <br/> | Type de base : entier, virgule flottante, etc. <br/> |



 

Les valeurs suivantes sont définies pour le type de base, bien que les outils Microsoft n’utilisent généralement pas ce champ et attribuent à LSB la valeur 0. Au lieu de cela, les informations de débogage Visual C++ sont utilisées pour indiquer les types. Toutefois, les valeurs COFF possibles sont répertoriées ici à des fins d’exhaustivité.



| Constante                             | Valeur          | Description                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| TYPE sym de l’IMAGE \_ \_ \_ null <br/>   | 0 <br/>  | Aucune information de type ou type de base inconnu. Les outils Microsoft utilisent ce paramètre <br/> |
| IMAGE \_ sym \_ type \_ void <br/>   | 1 <br/>  | Aucun type valide ; utilisé avec des pointeurs et des fonctions void <br/>                       |
| IMAGE \_ \_ type \_ char <br/>   | 2 <br/>  | Caractère (octet signé) <br/>                                                  |
| TYPE de sym d’IMAGE \_ \_ \_ short <br/>  | 3 <br/>  | Entier signé sur 2 octets <br/>                                                    |
| type de sym de l’IMAGE \_ \_ \_ int <br/>    | 4 <br/>  | Type entier népérien (normalement 4 octets dans Windows) <br/>                       |
| type de sym d’IMAGE \_ \_ \_ long <br/>   | 5 <br/>  | Entier signé sur 4 octets <br/>                                                    |
| TYPE sym de l’IMAGE \_ \_ \_ float <br/>  | 6 <br/>  | Nombre à virgule flottante sur 4 octets <br/>                                             |
| IMAGE \_ de \_ type sym \_ double <br/> | 7 <br/>  | Nombre à virgule flottante sur 8 octets <br/>                                            |
| \_structure de \_ type \_ sym de l’image <br/> | 8 <br/>  | Structure <br/>                                                                |
| IMAGE \_ de \_ type sym d’image \_ <br/>  | 9 <br/>  | Une Union <br/>                                                                    |
| \_enum de \_ type \_ sym de l’image <br/>   | 10 <br/> | Un type énuméré <br/>                                                         |
| IMAGE \_ sym \_ type \_ Marie <br/>    | 11 <br/> | Membre de l’énumération (une valeur spécifique) <br/>                                 |
| \_octet de \_ type \_ sym de l’image <br/>   | 12 <br/> | Octet ; entier non signé sur 1 octet <br/>                                            |
| IMAGE \_ \_ type de type sym \_ <br/>   | 13 <br/> | Un mot ; entier non signé sur 2 octets <br/>                                            |
| \_type sym d’image \_ \_ uint <br/>   | 14 <br/> | Entier non signé de taille naturelle (en principe, 4 octets) <br/>                    |
| TYPE de sym d’IMAGE \_ \_ \_ DWORD <br/>  | 15 <br/> | Entier non signé sur 4 octets <br/>                                                 |



 

L’octet le plus significatif spécifie si le symbole est un pointeur vers, un retour de fonction ou un tableau du type de base qui est spécifié dans le LSB. Les outils Microsoft utilisent ce champ uniquement pour indiquer si le symbole est une fonction, de sorte que les deux seules valeurs résultantes sont 0x0 et 0x20 pour le champ de type. Toutefois, d’autres outils peuvent utiliser ce champ pour communiquer plus d’informations.

Il est très important de spécifier correctement l’attribut de fonction. Ces informations sont nécessaires pour que les liens incrémentiels fonctionnent correctement. Pour certaines architectures, les informations peuvent être requises à d’autres fins.



| Constante                                | Valeur         | Description                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ sym \_ DTYPE \_ null <br/>     | 0 <br/> | Aucun type dérivé ; le symbole est une variable scalaire simple. <br/> |
| pointeur d’IMAGE \_ \_ DTYPE \_ <br/>  | 1 <br/> | Le symbole est un pointeur vers le type de base. <br/>                    |
| IMAGE \_ sym \_ DTYPE \_ fonction) <br/> | 2 <br/> | Le symbole est une fonction qui retourne un type de base. <br/>       |
| IMAGE \_ du \_ tableau DTYPE sym \_ <br/>    | 3 <br/> | Le symbole est un tableau de type de base. <br/>                     |



 

#### <a name="storage-class"></a>Classe de stockage

Le champ StorageClass de la table de symboles indique le type de définition représenté par un symbole. Le tableau suivant indique les valeurs possibles. Notez que le champ StorageClass est un entier non signé sur 1 octet. La valeur spéciale-1 doit donc être prise pour signifier son équivalent non signé, 0xFF.

Bien que le format COFF traditionnel utilise de nombreuses valeurs de classe de stockage, les outils Microsoft s’appuient sur Visual C++ format de débogage pour la plupart des informations symboliques et utilisent généralement uniquement quatre valeurs de classe de stockage : externe (2), statique (3), fonction (101) et fichier (103). Sauf dans le deuxième en-tête de colonne ci-dessous, « valeur » doit être utilisé pour signifier le champ de valeur de l’enregistrement de symboles (dont l’interprétation dépend du nombre trouvé comme classe de stockage).



| Constante                                          | Valeur                 | Description/interprétation du champ de valeur                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ fin \_ de la fonction de \_ classe sym de l’image <br/>  | -1 (0xFF) <br/> | Symbole spécial qui représente la fin de la fonction, à des fins de débogage. <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ sym, \_ classe \_ null <br/>               | 0 <br/>         | Aucune classe de stockage affectée. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ sym, \_ classe \_ automatique <br/>          | 1 <br/>         | Variable automatique (Stack). Le champ valeur spécifie le décalage du frame de pile. <br/>                                                                                                                                                                                                                                              |
| IMAGE \_ sym, \_ classe \_ External <br/>           | 2 <br/>         | Valeur que les outils Microsoft utilisent pour les symboles externes. Le champ valeur indique la taille si le numéro de section est une IMAGE \_ sym \_ non définie (0). Si le numéro de section n’est pas égal à zéro, le champ de valeur spécifie le décalage dans la section. <br/>                                                                                 |
| IMAGE \_ sym, \_ classe \_ statique <br/>             | 3 <br/>         | Décalage du symbole dans la section. Si le champ de valeur est égal à zéro, le symbole représente un nom de section. <br/>                                                                                                                                                                                                            |
| enregistrement de la \_ classe sym de l’image \_ \_ <br/>           | 4 <br/>         | Variable de registre. Le champ valeur spécifie le numéro du Registre. <br/>                                                                                                                                                                                                                                                            |
| IMAGE \_ sym \_ Class classe \_ externe \_ def <br/>      | 5 <br/>         | Symbole défini en externe. <br/>                                                                                                                                                                                                                                                                                           |
| étiquette de la \_ classe sym de l’image \_ \_ <br/>              | 6 <br/>         | Étiquette de code définie dans le module. Le champ valeur spécifie le décalage du symbole dans la section. <br/>                                                                                                                                                                                                         |
| étiquette de classe sym de l’IMAGE \_ \_ \_ non définie \_ <br/>   | 7 <br/>         | Référence à une étiquette de code qui n’est pas définie. <br/>                                                                                                                                                                                                                                                                               |
| IMAGE \_ \_ \_ membre de classe sym \_ de \_ struct <br/> | 8 <br/>         | Membre de la structure. Le champ valeur spécifie le n ième membre. <br/>                                                                                                                                                                                                                                                               |
| IMAGE \_ sym \_ , \_ argument de classe <br/>           | 9 <br/>         | Argument formel (paramètre) d’une fonction. Le champ valeur spécifie le n ième argument. <br/>                                                                                                                                                                                                                                      |
| IMAGE de la \_ \_ \_ \_ balise de structure de la classe sym <br/>        | 10 <br/>        | Entrée de nom de la balise de structure. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ \_ \_ membre de classe sym \_ de \_ Union <br/>  | 11 <br/>        | Membre Union. Le champ valeur spécifie le n ième membre. <br/>                                                                                                                                                                                                                                                                     |
| IMAGE \_ sym \_ Class \_ , \_ balise Union <br/>         | 12 <br/>        | Entrée de nom de balise d’Union. <br/>                                                                                                                                                                                                                                                                                                      |
| \_définition du \_ type de classe sym \_ de l’image \_ <br/>   | 13 <br/>        | Entrée typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| classe sym de l’IMAGE \_ \_ \_ static non défini \_ <br/>  | 14 <br/>        | Déclaration de données statiques. <br/>                                                                                                                                                                                                                                                                                                     |
| \_ \_ \_ balise enum de la classe sym de l’image \_ <br/>          | 15 <br/>        | Entrée de TagName de type énuméré. <br/>                                                                                                                                                                                                                                                                                              |
| IMAGE \_ \_ de classe \_ sym \_ de l' \_ enum <br/>   | 16 <br/>        | Membre d’une énumération. Le champ valeur spécifie le n ième membre. <br/>                                                                                                                                                                                                                                                         |
| IMAGE \_ sym \_ Class \_ Register \_ param <br/>    | 17 <br/>        | Paramètre Register. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ ( \_ \_ champ de bits de classe sym) \_ <br/>         | 18 <br/>        | Référence de champ de bits. Le champ valeur spécifie le n ième bit dans le champ de bits. <br/>                                                                                                                                                                                                                                                |
| IMAGE \_ ( \_ bloc de classe sym) \_ <br/>              | 100 <br/>       | Un enregistrement. BB (début de bloc) ou. EB (fin de bloc). Le champ valeur est l’adresse réadressable de l’emplacement du code. <br/>                                                                                                                                                                                                      |
| IMAGE \_ sym \_ ( \_ fonction de classe) <br/>           | 101 <br/>       | Valeur que les outils Microsoft utilisent pour les enregistrements de symboles qui définissent l’étendue d’une fonction : Begin Function (. BF), End Function (. EF) et les lignes de la fonction (. LF). Pour les enregistrements. LF, le champ valeur indique le nombre de lignes sources dans la fonction. Pour les enregistrements. EF, le champ valeur indique la taille du code de la fonction. <br/> |
| IMAGE \_ sym \_ Class \_ End \_ of \_ struct <br/>    | 102 <br/>       | Entrée de fin de structure. <br/>                                                                                                                                                                                                                                                                                                     |
| \_fichier de \_ classe \_ sym de l’image <br/>               | 103 <br/>       | Valeur que les outils Microsoft, ainsi que le format COFF traditionnel, utilisent pour l’enregistrement de symboles de fichier source. Le symbole est suivi des enregistrements auxiliaires qui désignent le nom du fichier. <br/>                                                                                                                                                       |
| IMAGE \_ sym \_ ( \_ section de classe) <br/>            | 104 <br/>       | Définition d’une section (les outils Microsoft utilisent la classe de stockage statique à la place). <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ sym \_ faible de la classe sym \_ \_ <br/>     | 105 <br/>       | Externe faible. Pour plus d’informations, consultez [format auxiliaire 3 : externes faibles](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| \_ \_ \_ jeton CLR de la classe sym de l’image \_ <br/>         | 107 <br/>       | Symbole de jeton CLR. Le nom est une chaîne ASCII qui se compose de la valeur hexadécimale du jeton. Pour plus d’informations, consultez [définition du jeton CLR (objet uniquement)](#clr-token-definition-object-only). <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Enregistrements de symboles auxiliaires

Les enregistrements de table de symboles auxiliaires suivent toujours, et s’appliquent à, un enregistrement de table de symboles standard. Un enregistrement auxiliaire peut avoir n’importe quel format que les outils peuvent reconnaître, mais 18 octets doivent leur être alloués afin que la table de symboles soit gérée comme un tableau de taille normale. Actuellement, les outils Microsoft reconnaissent les formats auxiliaires pour les types d’enregistrements suivants : les définitions de fonction, les symboles de début et de fin de fonction (. BF et. EF), les externes faibles, les noms de fichiers et les définitions de section.

La conception COFF traditionnelle comprend également des formats d’enregistrement auxiliaires pour les tableaux et les structures. Les outils Microsoft n’utilisent pas ceux-ci, mais placent plutôt ces informations symboliques dans Visual C++ format de débogage dans les sections de débogage.

#### <a name="auxiliary-format-1-function-definitions"></a>Format auxiliaire 1 : définitions de fonction

Un enregistrement de table de symboles marque le début d’une définition de fonction s’il a tous les éléments suivants : une classe de stockage externe (2), une valeur de type qui indique qu’il s’agit d’une fonction (0x20) et d’un numéro de section supérieur à zéro. Notez qu’un enregistrement de table de symboles ayant un numéro de section non défini (0) ne définit pas la fonction et n’a pas d’enregistrement auxiliaire. Les enregistrements de symboles de définition de fonction sont suivis d’un enregistrement auxiliaire dans le format décrit ci-dessous :



| Offset         | Taille          | Champ                             | Description                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Index de table de symboles de l’enregistrement de symbole. BF (Begin Function) correspondant. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Taille du code exécutable de la fonction elle-même. Si la fonction est dans sa propre section, le SizeOfRawData dans l’en-tête de la section est supérieur ou égal à ce champ, selon les considérations d’alignement. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | Décalage de fichier de la première entrée de numéro de ligne COFF pour la fonction, ou zéro si aucune n’existe. Pour plus d’informations, consultez [numéros de ligne COFF (déconseillé)](#coff-line-numbers-deprecated). <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Index de table de symboles de l’enregistrement pour la fonction suivante. Si la fonction est la dernière dans la table de symboles, ce champ a la valeur zéro. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Inutilisé <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Format auxiliaire 2 : symboles. BF et. EF

Pour chaque définition de fonction dans la table de symboles, trois éléments décrivent le début, la fin et le nombre de lignes. Chacun de ces symboles a une fonction de classe de stockage (101) :

Un enregistrement de symbole nommé. BF (fonction Begin). Le champ de valeur n’est pas utilisé.

Enregistrement de symbole nommé. LF (lignes dans la fonction). Le champ valeur indique le nombre de lignes dans la fonction.

Un enregistrement de symbole nommé. EF (End of Function). Le champ de valeur a le même nombre que le champ Taille totale de l’enregistrement de symboles de définition de fonction.

Les enregistrements de symboles. BF et. EF (mais pas les enregistrements. LF) sont suivis d’un enregistrement auxiliaire au format suivant :



| Offset         | Taille          | Champ                                         | Description                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Inutilisé <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | LineNumber <br/>                        | Nombre réel de lignes ordinales (1, 2, 3, etc.) dans le fichier source, correspondant à l’enregistrement. BF ou. EF. <br/>                                               |
| 6 <br/>  | 6 <br/> | Inutilisé <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (. BF uniquement) <br/> | Index de table de symboles de l’enregistrement de symbole BF suivant. Si la fonction est la dernière dans la table de symboles, ce champ a la valeur zéro. Elle n’est pas utilisée pour les enregistrements. EF. <br/> |
| 16 <br/> | 2 <br/> | Inutilisé <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Format auxiliaire 3 : externes faibles

Les « externes faibles » sont un mécanisme pour les fichiers objets qui permet la flexibilité au moment de la liaison. Un module peut contenir un symbole externe non résolu (sym1), mais il peut également inclure un enregistrement auxiliaire qui indique que si sym1 n’est pas présent au moment de la liaison, un autre symbole externe (sym2) est utilisé pour résoudre les références.

Si une définition de sym1 est liée, une référence externe au symbole est résolue normalement. Si une définition de sym1 n’est pas liée, toutes les références à l’externe faible pour sym1 font référence à sym2 à la place. Le symbole externe, sym2, doit toujours être lié ; en règle générale, il est défini dans le module qui contient la référence faible à sym1.

Les externes faibles sont représentés par un enregistrement de table de symboles avec une classe de stockage externe, un numéro de section UNDEF et une valeur de zéro. L’enregistrement de symboles faiblement externe est suivi d’un enregistrement auxiliaire au format suivant :



| Offset        | Taille           | Champ                       | Description                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | Index de table de symboles de sym2, le symbole à lier si sym1 est introuvable. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Caractéristiques <br/> | La valeur d’IMAGE \_ faible \_ extern \_ Search \_ nolibrary indique qu’aucune recherche de bibliothèque pour sym1 ne doit être effectuée. <br/> La valeur de la \_ bibliothèque de recherche extern faible d’image \_ \_ \_ indique qu’une recherche de bibliothèque pour sym1 doit être effectuée. <br/> La valeur d’un \_ alias de recherche extern faible d’image \_ \_ \_ indique que sym1 est un alias pour sym2. <br/> |
| 8 <br/> | 10 <br/> | Inutilisé <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Notez que le champ caractéristiques n’est pas défini dans WINNt. Manutention au lieu de cela, le champ Taille totale est utilisé.

#### <a name="auxiliary-format-4-files"></a>Format auxiliaire 4 : fichiers

Ce format suit un enregistrement de table de symboles avec le fichier de classe de stockage (103). Le nom du symbole doit être. file, et l’enregistrement auxiliaire qui le suit donne le nom d’un fichier de code source.



| Offset        | Taille           | Champ                 | Description                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Nom de fichier <br/> | Chaîne ANSI qui donne le nom du fichier source. Elle est complétée avec des valeurs NULL si elle est inférieure à la longueur maximale. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Format auxiliaire 5 : définitions de section

Ce format suit un enregistrement de table de symboles qui définit une section. Un enregistrement de ce type a un nom de symbole qui est le nom d’une section (par exemple,. Text ou. drectve) et dont la classe de stockage est STATIC (3). L’enregistrement auxiliaire fournit des informations sur la section à laquelle il fait référence. Par conséquent, elle duplique certaines des informations dans l’en-tête de la section.



| Offset         | Taille          | Champ                           | Description                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Longueur <br/>              | Taille des données de la section ; identique à SizeOfRawData dans l’en-tête de la section. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | Nombre d’entrées de réadressage pour la section. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Nombre d’entrées de numéro de ligne pour la section. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | EEPROM <br/>            | Somme de contrôle pour les données communes. Elle s’applique si l' \_ \_ indicateur COMDAT de l’image SCN LNK \_ est défini dans l’en-tête de la section. Pour plus d’informations, consultez la [section COMDAT sections (Object only)](#comdat-sections-object-only). <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Index de base un dans la table de section pour la section associée. Utilisé lorsque le paramètre de sélection COMDAT est défini sur 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Sélection <br/>           | Numéro de sélection COMDAT. Cela s’applique si la section est une section COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Inutilisé <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Sections COMDAT (objet uniquement)

Le champ de sélection du format auxiliaire de définition de section est applicable si la section est une section COMDAT. Une section COMDAT est une section qui peut être définie par plusieurs fichiers objets. (IMAGE \_ de l’indicateur \_ \_ Le COMDAT SCN lnk est défini dans le champ indicateurs de section de l’en-tête de la section.) Le champ de sélection détermine la façon dont l’éditeur de liens résout les multiples définitions des sections COMDAT.

Le premier symbole qui a la valeur de section de la section COMDAT doit être le symbole de section. Ce symbole porte le nom de la section, le champ de valeur égal à zéro, le numéro de section de la section COMDAT en question, le champ de type égal à IMAGE \_ sym \_ type \_ null, le champ de classe égal à image \_ sym \_ Class \_ static et un enregistrement auxiliaire. Le deuxième symbole est appelé « symbole COMDAT » et est utilisé par l’éditeur de liens conjointement avec le champ de sélection.

Les valeurs du champ de sélection sont affichées ci-dessous.



| Constante                                        | Valeur         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ COMDAT \_ Sélectionner des \_ nodoublons <br/> | 1 <br/> | Si ce symbole est déjà défini, l’éditeur de liens émet une erreur « multiplier le symbole défini ». <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ COMDAT \_ sélectionner \_ any <br/>          | 2 <br/> | Toute section qui définit le même symbole COMDAT peut être liée ; le reste est supprimé. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT- \_ Sélectionner la \_ même \_ taille <br/>   | 3 <br/> | L’éditeur de liens choisit une section arbitraire parmi les définitions de ce symbole. Si toutes les définitions ne sont pas de la même taille, une erreur « multiplier le symbole défini » est émise. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ COMDAT \_ sélectionner \_ la \_ correspondance exacte <br/> | 4 <br/> | L’éditeur de liens choisit une section arbitraire parmi les définitions de ce symbole. Si toutes les définitions ne correspondent pas exactement, une erreur « multiplier le symbole défini » est émise. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ Select \_ associatif <br/>  | 5 <br/> | La section est liée si une certaine section COMDAT est liée. Cette autre section est indiquée par le champ numéro de l’enregistrement de symbole auxiliaire pour la définition de section. Ce paramètre est utile pour les définitions qui ont des composants dans plusieurs sections (par exemple, du code dans un et des données d’un autre), mais où tous doivent être liés ou ignorés comme un ensemble. L’autre section à laquelle cette section est associée doit être une section COMDAT, qui peut être une autre section COMDAT associative. Une chaîne d’association de section de la section COMDAT associatif ne peut pas former une boucle. La chaîne d’association de la section doit finalement arriver dans une section COMDAT qui n’a pas d’IMAGE \_ COMDAT \_ Select \_ associatif Set. <br/> |
| IMAGE \_ COMDAT \_ Select le \_ plus grand <br/>      | 6 <br/> | L’éditeur de liens choisit la plus grande définition parmi toutes les définitions de ce symbole. Si plusieurs définitions ont cette taille, le choix entre elles est arbitraire. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Définition du jeton CLR (objet uniquement)

Ce symbole auxiliaire suit généralement le jeton CLR de la classe sym de l’IMAGE \_ \_ \_ \_ . Elle est utilisée pour associer un jeton à l’espace de noms de la table de symboles COFF.



| Offset        | Taille           | Champ                        | Description                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Doit être une \_ \_ \_ définition de jeton au type de symbole à image \_ \_ (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Réservé, doit être égal à zéro. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Index de symboles du symbole COFF auquel cette définition de jeton CLR fait référence. <br/> |
| 6 <br/> | 12 <br/> |                              | Réservé, doit être égal à zéro. <br/>                                                        |



 

### <a name="coff-string-table"></a>Table de chaînes COFF

La table de caractères COFF juste après la table de symboles COFF. La position de cette table est trouvée en acceptant l’adresse de la table de symboles dans l’en-tête COFF et en ajoutant le nombre de symboles multiplié par la taille d’un symbole.

Au début de la table de chaînes COFF se trouvent 4 octets qui contiennent la taille totale (en octets) du reste de la table de chaînes. Cette taille comprend le champ taille lui-même, de sorte que la valeur de cet emplacement est de 4 Si aucune chaîne n’était présente.

Après la taille, les chaînes se terminant par un caractère NULL sont pointées par des symboles dans la table de symboles COFF.

### <a name="the-attribute-certificate-table-image-only"></a>Table de certificats d’attribut (image uniquement)

Les certificats d’attribut peuvent être associés à une image en ajoutant une table de certificats d’attribut. La table des certificats d’attribut est composée d’un ensemble d’entrées de certificat d’attribut contiguës, alignées sur le mot quadruple. Le remplissage à zéro est inséré entre la fin d’origine du fichier et le début de la table de certificats d’attribut pour atteindre cet alignement. Chaque entrée de certificat d’attribut contient les champs suivants.



| Offset       | Taille                         | Champ                       | Description                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Spécifie la longueur de l’entrée de certificat d’attribut. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contient le numéro de version du certificat. Pour plus d’informations, consultez le texte suivant.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Spécifie le type de contenu dans bCertificate. Pour plus d’informations, consultez le texte suivant.<br/>             |
| 8<br/> | Consultez<br/> | bCertificate<br/>     | Contient un certificat, tel qu’une signature Authenticode. Pour plus d’informations, consultez le texte suivant.<br/> |



 

La valeur d’adresse virtuelle de l’entrée de table de certificats dans le répertoire de données d’en-tête facultatif est un décalage de fichier par rapport à la première entrée de certificat d’attribut. Les entrées suivantes sont accessibles en avançant les octets dwLength de cette entrée, arrondis à un multiple de 8 octets, à partir du début de l’entrée de certificat attribut actuel. Cela se poursuit jusqu’à ce que la somme des valeurs de dwLength arrondies soit égale à la valeur de taille de l’entrée de table de certificats dans le répertoire de données d’en-tête facultatif. Si la somme des valeurs de dwLength arrondies n’est pas égale à la valeur de taille, la table de certificats d’attribut ou le champ de taille est endommagé.

Par exemple, si l’entrée de table de certificats du répertoire de données d’en-tête facultatif contient :


```C++
virtual address = 0x5000
size = 0x1000
```



Le premier certificat commence à l’offset 0x5000 à partir du début du fichier sur le disque. Pour passer en revue toutes les entrées de certificat d’attribut :

1.  Ajoutez la valeur dwLength du premier certificat d’attribut au décalage de départ.
2.  Arrondit la valeur de l’étape 1 au multiple de 8 octets le plus proche pour rechercher le décalage de la deuxième entrée de certificat d’attribut.
3.  Ajoutez la valeur de décalage de l’étape 2 à la valeur dwLength de l’entrée de certificat du deuxième attribut et arrondissez au multiple de 8 octets le plus proche pour déterminer le décalage de la troisième entrée de certificat d’attribut.
4.  Répétez l’étape 3 pour chaque certificat successif jusqu’à ce que le décalage calculé soit égal à 0x6000 (0x5000 Start + 0x1000 total size), ce qui indique que vous avez parcouru la totalité de la table.

Vous pouvez également énumérer les entrées de certificat en appelant la fonction Win32 **ImageEnumerateCertificates** dans une boucle. Pour obtenir un lien vers la page de référence de la fonction, consultez [références](#references).

Les entrées de la table de certificats d’attribut peuvent contenir n’importe quel type de certificat, à condition que l’entrée ait la valeur dwLength correcte, une valeur wRevision unique et une valeur wCertificateType unique. Le type le plus courant de l’entrée de table de certificats est une \_ structure de certificat Win, qui est documentée dans wintrust. h et traitée dans le reste de cette section.

Les options du \_ membre **wRevision** du certificat Win incluent (mais ne sont pas limitées à) ce qui suit.



| Valeur             | Nom                                 | Notes                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | \_Révision du certificat Win \_ \_ 1 \_ 0<br/> | Version 1, version héritée de la \_ structure de certificat Win. Il est pris en charge uniquement à des fins de vérification des signatures Authenticode héritées.<br/> |
| 0x0200<br/> | \_Révision du certificat Win \_ \_ 2 \_ 0<br/> | La version 2 est la version actuelle de la \_ structure de certificat Win. <br/>                                                                       |



 

Les options du \_ membre **wCertificateType** du certificat Win incluent (sans s’y limiter) les éléments du tableau suivant. Notez que certaines valeurs ne sont pas prises en charge actuellement.



| Valeur             | Nom                                           | Notes                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | \_Type de certificat Win \_ \_ x509 <br/>              | bCertificate contient un certificat X. 509 <br/> Non pris en charge<br/>         |
| 0x0002<br/> | \_type de certificat Win \_ \_ \_ données signées par PKCS \_<br/> | bCertificate contient une \# structure SIGNEDDATA PKCS 7<br/>                         |
| 0x0003<br/> | \_Type de certificat Win \_ \_ réservé \_ 1<br/>        | Réservé <br/>                                                                    |
| 0x0004<br/> | TYPE de certificat WIN signé pour la \_ \_ \_ \_ pile TS \_<br/>  | Signature de certificat de la pile de protocole Terminal Server <br/> Non pris en charge<br/> |



 

Le \_ membre **bCertificate** de la structure de certificat Win contient un tableau d’octets de longueur variable avec le type de contenu spécifié par **wCertificateType**. Le type pris en charge par Authenticode est WIN \_ Certificate \_ type \_ PKCS \_ \_ Data signature, une \# structure PKCS 7 **SignedData** . pour plus d’informations sur le format de signature numérique authenticode, consultez [Windows format de signature d’exécutable Portable authenticode](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Si le contenu **bCertificate** ne se termine pas par une limite de mot quadruple, l’entrée de certificat d’attribut est complétée par des zéros, de la fin de **bCertificate** à la limite de mot quadruple suivante.

La valeur **dwLength** est la longueur de la structure de certificat Win finalisée \_ et est calculée comme suit :

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Cette longueur doit inclure la taille de tout remplissage qui est utilisé pour répondre à l’exigence selon laquelle chaque \_ structure de certificat Win est alignée à mot quadruple :

` dwLength += (8 - (dwLength & 7)) & 7;`

Taille de la **table de certificats**-spécifiée dans l’entrée de **table de certificats** dans les [répertoires de données d’en-tête facultatifs (image uniquement)](#optional-header-data-directories-image-only)-comprend le remplissage.

Pour plus d’informations sur l’utilisation de l’API ImageHlp pour énumérer, ajouter et supprimer des certificats dans des fichiers PE, consultez [fonctions ImageHlp](imagehlp-functions.md).

#### <a name="certificate-data"></a>Données du certificat

Comme indiqué dans la section précédente, les certificats de la table des certificats d’attribut peuvent contenir n’importe quel type de certificat. Les certificats qui garantissent l’intégrité d’un fichier PE peuvent inclure un hachage d’image PE.

Un hachage d’image PE (ou hachage de fichier) est similaire à une somme de contrôle de fichier dans le fait que l’algorithme de hachage produit un résumé de message lié à l’intégrité d’un fichier. Toutefois, une somme de contrôle est produite par un algorithme simple et est principalement utilisée pour détecter si un bloc de mémoire sur le disque a disparu et que les valeurs stockées sont endommagées. Un hachage de fichier est similaire à une somme de contrôle en ce qu’il détecte également une altération de fichier. Toutefois, contrairement à la plupart des algorithmes de somme de contrôle, il est très difficile de modifier un fichier sans modifier le hachage de fichier à partir de sa valeur non modifiée d’origine. Un hachage de fichier peut donc être utilisé pour détecter les modifications intentionnelles et même subtiles d’un fichier, telles que celles introduites par les virus, les pirates ou les chevaux de Troie.

Lorsqu’il est inclus dans un certificat, le condensé d’image doit exclure certains champs de l’image PE, tels que la somme de contrôle et l’entrée de la table de certificats dans les répertoires de données d’en-tête facultatifs. Cela est dû au fait que l’ajout d’un certificat modifie ces champs et provoque le calcul d’une valeur de hachage différente.

La fonction Win32 **ImageGetDigestStream** fournit un flux de données à partir d’un fichier PE cible avec lequel hacher les fonctions. Ce flux de données reste cohérent lors de l’ajout ou de la suppression de certificats dans un fichier PE. En fonction des paramètres transmis à **ImageGetDigestStream**, d’autres données de l’image PE peuvent être omises dans le calcul de hachage. Pour obtenir un lien vers la page de référence de la fonction, consultez [références](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importer des tables (image uniquement)

Ces tables ont été ajoutées à l’image pour prendre en charge un mécanisme uniforme permettant aux applications de retarder le chargement d’une DLL jusqu’au premier appel de cette DLL. La disposition des tables correspond à celle des tables d’importation traditionnelles qui sont décrites dans la section 6,4, [la section. idata](#the-idata-section).» Seuls quelques détails sont présentés ici.

#### <a name="the-delay-load-directory-table"></a>Table Delay-Load Directory

La table de répertoire de chargement différé est l’équivalent de la table d’importation des répertoires. Il peut être récupéré via l’entrée retarder le descripteur d’importation dans la liste des répertoires de données d’en-tête facultatifs (décalage 200). La table est organisée comme suit :



| Offset         | Taille          | Champ                                  | Description                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Attributs <br/>                 | Doit être zéro. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Name <br/>                       | Adresse RVA du nom de la DLL à charger. Le nom se trouve dans la section données en lecture seule de l’image. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Handle de module <br/>              | RVA du handle de module (dans la section de données de l’image) de la DLL à charger différée. Elle est utilisée pour le stockage par la routine fournie pour gérer le chargement différé. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Différer la table d’adresses d’importation <br/> | Adresse RVA de la table d’adresses d’importation à chargement différé. Pour plus d’informations, consultez [retarder la table d’adresses d’importation (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Retarder la table du nom d’importation <br/>    | RVA de la table de noms de chargement différé, qui contient les noms des importations qui devront peut-être être chargées. Cela correspond à la disposition de la table du nom d’importation. Pour plus d’informations, consultez [table Hint/Name](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Table d’importation à retard liée <br/>   | Adresse RVA de la table d’adresses de chargement différée liée, si elle existe. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Décharger la table d’importation <br/>  | Adresse RVA de la table d’adresses de chargement différé, si elle existe. Il s’agit d’une copie exacte de la table des adresses d’importation différée. Si l’appelant décharge la DLL, cette table doit être recopiée sur la table d’adresses d’importation différée afin que les appels suivants à la DLL continuent d’utiliser correctement le mécanisme de thunk. <br/> |
| 28 <br/> | 4 <br/> | Horodatage <br/>                 | Horodateur de la DLL à laquelle cette image a été liée. <br/>                                                                                                                                                                                                                                                     |



 

Les tables référencées dans cette structure de données sont organisées et triées comme leurs équivalents pour les importations traditionnelles. Pour plus d’informations, consultez [la section. idata](#the-idata-section).

#### <a name="attributes"></a>Attributs

Comme encore, aucun indicateur d’attribut n’est défini. L’éditeur de liens définit ce champ sur zéro dans l’image. Ce champ peut être utilisé pour étendre l’enregistrement en indiquant la présence de nouveaux champs, ou il peut être utilisé pour indiquer des comportements aux fonctions d’assistance Delay ou Unload.

#### <a name="name"></a>Name

Le nom de la DLL à charger différée réside dans la section des données en lecture seule de l’image. Elle est référencée via le champ szName.

#### <a name="module-handle"></a>Handle de module

Le handle de la DLL à charger différée se trouve dans la section des données de l’image. Le champ phmod pointe vers le handle. Le programme d’assistance au chargement différé fourni utilise cet emplacement pour stocker le descripteur dans la DLL chargée.

#### <a name="delay-import-address-table"></a>Différer la table d’adresses d’importation

La table d’adresses d’importation (IAT) Delay est référencée par le descripteur d’importation Delay via le champ pIAT. L’application d’assistance de chargement différé met à jour ces pointeurs avec les points d’entrée réels afin que les thunks ne soient plus dans la boucle d’appel. Les pointeurs de fonction sont accessibles à l’aide de l’expression `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Retarder la table du nom d’importation

La table de noms d’importation différée (INT) contient les noms des importations qui peuvent nécessiter un chargement. Elles sont triées de la même façon que les pointeurs de fonction dans l’IAT. Ils se composent des mêmes structures que la norme INT et sont accessibles à l’aide de l’expression `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Table d’adresses d’importation à liaison différée et horodatage

La table d’adresses d’importation à liaison différée (BIAT) est une table facultative d’éléments de données de THUNK d’IMAGE \_ \_ qui est utilisée avec le champ d’horodatage de la table de répertoire de chargement différé par une phase de liaison post-traitement.

#### <a name="delay-unload-import-address-table"></a>Différer la table d’adresses d’importation

La table d’adresses d’importation de déchargement différée (UIAT) est une table facultative d’éléments de données de THUNK d’IMAGE \_ \_ que le code de déchargement utilise pour gérer une demande de déchargement explicite. Il se compose de données initialisées dans la section en lecture seule qui est une copie exacte de la IAT d’origine qui a désigné le code pour les thunks de chargement différé. Sur la demande de déchargement, la bibliothèque peut être libérée, le \* phmod effacé et le UIAT écrit sur l’IAT pour restaurer tous les éléments à l’État préchargé.

## <a name="special-sections"></a>Sections spéciales

- [La section. Debug](#the-debug-section)
  - [Répertoire de débogage (image uniquement)](#debug-directory-image-only)
  - [Type de débogage](#debug-type)
  - [. Debug $ F (objet uniquement)](#debugf-object-only)
  - [. déboguer $ S (objet uniquement)](#debugs-object-only)
  - [. Debug $ P (objet uniquement)](#debugp-object-only)
  - [. Debug $ T (objet uniquement)](#debugt-object-only)
  - [Prise en charge de l’éditeur de liens pour les informations de débogage Microsoft](#linker-support-for-microsoft-debug-information)
- [Section. drectve (objet uniquement)](#the-drectve-section-object-only)
- [Section. edata (image uniquement)](#the-edata-section-image-only)
  - [Exporter une table de répertoire](#export-directory-table)
  - [Exporter une table d’adresses](#export-address-table)
  - [Exporter le nom de la table de pointeurs](#export-name-pointer-table)
  - [Exporter une table ordinale](#export-ordinal-table)
  - [Exporter le nom table](#export-name-table)
- [Section. idata](#the-idata-section)
  - [Importer une table de répertoire](#import-directory-table)
  - [Importer une table de recherche](#import-lookup-table)
  - [Table Hint/Name](#hintname-table)
  - [Table d’adresses d’importation](#delay-import-address-table)
- [La section. pdata](#the-pdata-section)
- [Section. reloc (image uniquement)](#the-reloc-section-image-only)
  - [Bloc de réadressage de base](#base-relocation-block)
  - [Types de réadressage de base](#base-relocation-types)
- [Section. TLS](#the-tls-section)
  - [Le répertoire TLS](#the-tls-directory)
  - [Fonctions de rappel TLS](#tls-callback-functions)
- [Structure de la configuration de charge (image uniquement)](#the-load-configuration-structure-image-only)
  - [Charger le répertoire de configuration](#load-configuration-directory)
  - [Charger la disposition de configuration](#load-configuration-layout)
- [Section. rsrc](#the-rsrc-section)
  - [Table de répertoire des ressources](#resource-directory-table)
  - [Entrées de répertoire de ressources](#resource-directory-entries)
  - [Chaîne du répertoire de ressources](#resource-directory-string)
  - [Entrée de données de ressource](#resource-data-entry)
- [Section. cormeta (objet uniquement)](#the-cormeta-section-object-only)
- [Section. sxdata](#the-sxdata-section)

Les sections COFF classiques contiennent du code ou des données que les liens et les chargeurs Microsoft Win32 traitent sans connaissance particulière du contenu de la section. Le contenu s’applique uniquement à l’application en cours de liaison ou d’exécution.

Toutefois, certaines sections COFF ont des significations spéciales lorsqu’elles se trouvent dans des fichiers objets ou des fichiers image. Les outils et les chargeurs reconnaissent ces sections, car ils ont des indicateurs spéciaux définis dans l’en-tête de la section, car des emplacements spéciaux dans l’en-tête facultatif de l’image pointent vers eux, ou parce que le nom de la section lui-même indique une fonction spéciale de la section. (Même si le nom de la section lui-même n’indique pas une fonction spéciale de la section, le nom de la section est dicté par Convention, de sorte que les auteurs de cette spécification peuvent faire référence à un nom de section dans tous les cas.)

Les sections réservées et leurs attributs sont décrits dans le tableau ci-dessous, suivis des descriptions détaillées des types de sections qui sont conservés dans les fichiers exécutables et des types de section qui contiennent des métadonnées pour les extensions.



| Nom de la section          | Content                                                                                                                                                                  | Caractéristiques                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| . BSS <br/>      | Données non initialisées (format libre) <br/>                                                                                                                             | IMAGE \_ SCN \_ CNT \_ non initialisé image de données non initialisées SCN \_ \| \_ \_ MEM \_ lecture \| image \_ mémoire SCN en \_ \_ écriture <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Métadonnées CLR qui indiquent que le fichier objet contient du code managé <br/>                                                                                       | IMAGE \_ SCN \_ LNK \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . Data <br/>     | Données initialisées (format libre) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ données initialisées \_ image de données \| \_ SCN \_ mém \_ lecture \| image \_ mémoire SCN en \_ \_ écriture SCN <br/>                                                                                                                                                                                                                                                                                                 |
| . débogage $ F <br/>  | Informations de débogage FPO générées (objet uniquement, architecture x86 uniquement et désormais obsolètes) <br/>                                                                       | IMAGE \_ SCN \_ CNT \_ d’image de données initialisée SCN \_ \| \_ \_ mém \_ lecture d’image de lecture d' \| image \_ SCN \_ MEM \_ Ignorable <br/>                                                                                                                                                                                                                                                                                           |
| . débogage $ P <br/>  | Types de débogage précompilés (objet uniquement) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT \_ d’image de données initialisée SCN \_ \| \_ \_ mém \_ lecture d’image de lecture d' \| image \_ SCN \_ MEM \_ Ignorable <br/>                                                                                                                                                                                                                                                                                           |
| . déboguer $ S <br/>  | Symboles de débogage (objet uniquement) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT \_ d’image de données initialisée SCN \_ \| \_ \_ mém \_ lecture d’image de lecture d' \| image \_ SCN \_ MEM \_ Ignorable <br/>                                                                                                                                                                                                                                                                                           |
| . débogage $ T <br/>  | Types de débogage (objet uniquement) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT \_ d’image de données initialisée SCN \_ \| \_ \_ mém \_ lecture d’image de lecture d' \| image \_ SCN \_ MEM \_ Ignorable <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Options de l’éditeur de liens <br/>                                                                                                                                               | IMAGE \_ SCN \_ LNK \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Exporter les tables <br/>                                                                                                                                                | IMAGE \_ de \_ données d’initialisation de l’image SCN CNT- \_ \_ \| \_ \_ mémoire SCN \_ en lecture <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importer des tables <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ données initialisées \_ image de données \| \_ SCN \_ mém \_ lecture \| image \_ mémoire SCN en \_ \_ écriture SCN <br/>                                                                                                                                                                                                                                                                                                 |
| . idlsym <br/>   | Comprend les attributs SEH inscrits (image uniquement) pour prendre en charge les attributs IDL. Pour plus d’informations, consultez « Attributs IDL » dans [références](#references) à la fin de cette rubrique. <br/> | IMAGE \_ SCN \_ LNK \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . pdata <br/>    | Informations sur l’exception <br/>                                                                                                                                        | IMAGE \_ de \_ données d’initialisation de l’image SCN CNT- \_ \_ \| \_ \_ mémoire SCN \_ en lecture <br/>                                                                                                                                                                                                                                                                                                                           |
| . rdata <br/>    | Données initialisées en lecture seule <br/>                                                                                                                                   | IMAGE \_ de \_ données d’initialisation de l’image SCN CNT- \_ \_ \| \_ \_ mémoire SCN \_ en lecture <br/>                                                                                                                                                                                                                                                                                                                           |
| . reloc <br/>    | Réadressages d’images <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT \_ d’image de données initialisée SCN \_ \| \_ \_ mém \_ lecture d’image de lecture d' \| image \_ SCN \_ MEM \_ Ignorable <br/>                                                                                                                                                                                                                                                                                           |
| . rsrc <br/>     | Répertoire de ressources <br/>                                                                                                                                           | IMAGE \_ de \_ données d’initialisation de l’image SCN CNT- \_ \_ \| \_ \_ mémoire SCN \_ en lecture <br/>                                                                                                                                                                                                                                                                                                                           |
| . sbss <br/>     | Données non initialisées relatives à GP (format libre) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT \_ non initialisé image \_ \| de données \_ SCN \_ MEM \_ lecture IMAGE SCN \| \_ \_ MEM \_ écriture \| image \_ SCN \_ GPREL l’image \_ SCN \_ GPREL Flag doit être définie pour les architectures IA64 uniquement. cet indicateur n’est pas valide pour les autres architectures. L' \_ \_ indicateur GPREL SCN de l’image concerne uniquement les fichiers objets ; lorsque ce type de section apparaît dans un fichier image, l' \_ Indicateur SCN GPREL de l’image \_ ne doit pas être défini. <br/> |
| . sdata <br/>    | Données initialisées par rapport à GP (format libre) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT avec \_ initialisation initialisation image \_ \| de données \_ SCN mém lire image SCN \_ \_ \| \_ \_ MEM \_ écriture \| image \_ SCN \_ GPREL l’image \_ SCN \_ GPREL Flag doit être définie pour les architectures IA64 uniquement. cet indicateur n’est pas valide pour les autres architectures. L' \_ \_ indicateur GPREL SCN de l’image concerne uniquement les fichiers objets ; lorsque ce type de section apparaît dans un fichier image, l' \_ Indicateur SCN GPREL de l’image \_ ne doit pas être défini. <br/>   |
| .srdata <br/>   | Données en lecture seule relatives à GP (format libre) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT avec \_ initialisation d’image \_ \| de données \_ SCN \_ mém \_ lecture \| \_ d’image SCN \_ GPREL l' \_ indicateur d’image SCN \_ GPREL doit être défini pour les architectures IA64 uniquement. cet indicateur n’est pas valide pour les autres architectures. L' \_ \_ indicateur GPREL SCN de l’image concerne uniquement les fichiers objets ; lorsque ce type de section apparaît dans un fichier image, l' \_ Indicateur SCN GPREL de l’image \_ ne doit pas être défini. <br/>                             |
| .sxdata <br/>   | Données du gestionnaire d’exceptions inscrit (format libre et x86/objet uniquement) <br/>                                                                                          | IMAGE \_ SCN \_ LNK \_ info contient l’index de symboles de chacun des gestionnaires d’exceptions référencés par le code dans ce fichier objet. Le symbole peut être pour un symbole UNDEF ou un symbole défini dans ce module. <br/>                                                                                                                                                                     |
| .text <br/>     | Code exécutable (format libre) <br/>                                                                                                                                | IMAGE de code d’image \_ SCN \_ CNT \_ \| \_ SCN \_ MEM \_ Execute \| IIMAGE \_ SCN \_ MEM \_ Read <br/>                                                                                                                                                                                                                                                                                                           |
| . TLS <br/>      | Stockage local des threads (objet uniquement) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ données initialisées \_ image de données \| \_ SCN \_ mém \_ lecture \| image \_ mémoire SCN en \_ \_ écriture SCN <br/>                                                                                                                                                                                                                                                                                                 |
| . TLS $ <br/>     | Stockage local des threads (objet uniquement) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ données initialisées \_ image de données \| \_ SCN \_ mém \_ lecture \| image \_ mémoire SCN en \_ \_ écriture SCN <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | Données initialisées par rapport à GP (format libre et pour les architectures ARM, SH4 et Thumb uniquement) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ données initialisées \_ image de données \| \_ SCN \_ mém \_ lecture \| image \_ mémoire SCN en \_ \_ écriture SCN <br/>                                                                                                                                                                                                                                                                                                 |
| . XData <br/>    | Informations sur l’exception (format libre) <br/>                                                                                                                          | IMAGE \_ de \_ données d’initialisation de l’image SCN CNT- \_ \_ \| \_ \_ mémoire SCN \_ en lecture <br/>                                                                                                                                                                                                                                                                                                                           |



 

Certaines des sections répertoriées ici sont marquées « objet uniquement » ou « image uniquement » pour indiquer que leur sémantique spéciale est pertinente uniquement pour les fichiers objets ou les fichiers image, respectivement. Une section marquée « image only » peut toujours apparaître dans un fichier objet comme un moyen d’accéder au fichier image, mais la section n’a aucune signification particulière pour l’éditeur de liens, mais uniquement pour le chargeur de fichiers image.

### <a name="the-debug-section"></a>La section. Debug

La section. Debug est utilisée dans les fichiers objets pour contenir des informations de débogage générées par le compilateur et dans des fichiers image pour contenir toutes les informations de débogage générées. Cette section décrit l’empaquetage des informations de débogage dans des fichiers objets et image.

La section suivante décrit le format du répertoire de débogage, qui peut se trouver n’importe où dans l’image. Les sections suivantes décrivent les « groupes » dans les fichiers objets qui contiennent des informations de débogage.

La valeur par défaut de l’éditeur de liens est que les informations de débogage ne sont pas mappées dans l’espace d’adressage de l’image. Une section. Debug existe uniquement lorsque des informations de débogage sont mappées dans l’espace d’adressage.

#### <a name="debug-directory-image-only"></a>Répertoire de débogage (image uniquement)

Les fichiers image contiennent un répertoire de débogage facultatif qui indique la forme des informations de débogage qui sont présentes et leur emplacement. Ce répertoire se compose d’un tableau d’entrées de répertoire de débogage dont l’emplacement et la taille sont indiqués dans l’en-tête facultatif de l’image.

Le répertoire de débogage peut être dans une section pouvant être supprimée. Debug (le cas échéant), ou il peut être inclus dans une autre section du fichier image, ou ne pas figurer dans une section.

Chaque entrée de répertoire de débogage identifie l’emplacement et la taille d’un bloc d’informations de débogage. L’adresse RVA spécifiée peut être égale à zéro si les informations de débogage ne sont pas couvertes par un en-tête de section (autrement dit, elle réside dans le fichier image et n’est pas mappée dans l’espace d’adressage au moment de l’exécution). Si elle est mappée, l’adresse RVA est son adresse.

Une entrée de répertoire de débogage a le format suivant :



| Offset         | Taille          | Champ                        | Description                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caractéristiques <br/>  | Réservé, doit être égal à zéro. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Heure et date de création des données de débogage. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Numéro de version principale du format de données de débogage. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Numéro de version mineure du format de données de débogage. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Type <br/>             | Format des informations de débogage. Ce champ permet la prise en charge de plusieurs débogueurs. Pour plus d’informations, consultez [type de débogage](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Taille des données de débogage (sans inclure le répertoire de débogage lui-même). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | Adresse des données de débogage en cas de chargement, par rapport à la base de l’image. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Pointeur de fichier vers les données de débogage. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Type de débogage

Les valeurs suivantes sont définies pour le champ type de l’entrée de répertoire de débogage :



| Constante                                        | Valeur          | Description                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_type de débogage d’image \_ \_ inconnu <br/>         | 0 <br/>  | Valeur inconnue qui est ignorée par tous les outils. <br/>                                                                                                                                                       |
| \_type de débogage d’image \_ \_ COFF <br/>            | 1 <br/>  | Informations de débogage COFF (numéros de ligne, table de symboles et table de chaînes). Ce type d’informations de débogage est également désigné par des champs dans les en-têtes de fichiers. <br/>                                          |
| \_type de débogage d’image \_ \_ CODEVIEW <br/>        | 2 <br/>  | Informations de débogage Visual C++. <br/>                                                                                                                                                                    |
| \_type de débogage d’image \_ \_ FPO <br/>             | 3 <br/>  | Informations d’omission du pointeur de frame (FPO). Ces informations indiquent au débogueur comment interpréter les frames de pile non standard, qui utilisent le registre EBP à une autre fin que comme pointeur de frame. <br/> |
| \_type de débogage d’image \_ \_ misc <br/>            | 4 <br/>  | Emplacement du fichier DBG. <br/>                                                                                                                                                                            |
| \_exception de type de débogage d’image \_ \_ <br/>       | 5 <br/>  | Copie de la section. pData. <br/>                                                                                                                                                                            |
| \_Correction du type de débogage de l’image \_ \_ <br/>           | 6 <br/>  | Réservé. <br/>                                                                                                                                                                                            |
| \_ \_ type de débogage d’image \_ OMAP \_ vers \_ src <br/>   | 7 <br/>  | Mappage d’un RVA dans image à un RVA dans l’image source. <br/>                                                                                                                                          |
| \_ \_ type de débogage d’image \_ OMAP \_ à partir de \_ src <br/> | 8 <br/>  | Mappage d’un RVA dans l’image source à un RVA dans l’image. <br/>                                                                                                                                          |
| \_type de débogage d’image \_ \_ Borland <br/>         | 9 <br/>  | Réservé pour Borland. <br/>                                                                                                                                                                                |
| \_Type de débogage d’image \_ \_ RESERVED10 <br/>      | 10 <br/> | Réservé. <br/>                                                                                                                                                                                            |
| \_type de débogage d’image \_ \_ CLSID <br/>           | 11 <br/> | Réservé. <br/>                                                                                                                                                                                            |
| \_reproduction de type de débogage d’image \_ \_ <br/>           | 16 <br/> | Déterminisme ou reproductibilité PE. <br/>                                                                                                                                                                   |
| \_type de débogage d’image \_ \_ ex \_ DLLCHARACTERISTICS | 20 | Caractéristiques des DLL étendues. |



 

Si le champ type est défini sur IMAGE \_ Debug \_ type \_ FPO, les données brutes de débogage sont un tableau dans lequel chaque membre décrit le frame de pile d’une fonction. Toutes les fonctions du fichier image ne doivent pas avoir d’informations FPO définies, même si le type de débogage est FPO. Les fonctions qui n’ont pas d’informations FPO sont supposées avoir des frames de pile normaux. Le format des informations FPO est le suivant :


```C++
#define FRAME_FPO   0               
#define FRAME_TRAP  1
#define FRAME_TSS   2
               
typedef struct _FPO_DATA {
    DWORD       ulOffStart;            // offset 1st byte of function code
    DWORD       cbProcSize;            // # bytes in function
    DWORD       cdwLocals;             // # bytes in locals/4
    WORD        cdwParams;             // # bytes in params/4
    WORD        cbProlog : 8;          // # bytes in prolog
    WORD        cbRegs   : 3;          // # regs saved
    WORD        fHasSEH  : 1;          // TRUE if SEH in func
    WORD        fUseBP   : 1;          // TRUE if EBP has been allocated
    WORD        reserved : 1;          // reserved for future use
    WORD        cbFrame  : 2;          // frame type
} FPO_DATA;
```



La présence d’une entrée de type IMAGE de \_ débogage de type \_ \_ reproduction indique que le fichier PE est généré de manière à atteindre le déterminisme ou la reproductibilité. Si l’entrée n’est pas modifiée, le fichier PE de sortie est garanti comme étant un bit-bit identique, quel que soit l’endroit où le PE est produit. Divers champs de datage de date et d’heure dans le fichier PE sont remplis avec une partie ou l’ensemble des bits d’une valeur de hachage calculée qui utilise le contenu de fichier PE comme entrée, et par conséquent, ne représentent plus la date et l’heure réelles auxquelles un fichier PE ou des données spécifiques associées dans le PE sont produits. Les données brutes de cette entrée de débogage peuvent être vides ou peuvent contenir une valeur de hachage calculée précédée d’une valeur de quatre octets qui représente la longueur de la valeur de hachage.

Si le champ type est défini sur IMAGE \_ Debug \_ type \_ ex \_ DLLCHARACTERISTICS, les données brutes de débogage contiennent des bits de caractéristiques de dll étendues, en plus de celles qui peuvent être définies dans l’en-tête facultatif de l’image. Consultez les caractéristiques de la [dll](#dll-characteristics) dans la section [en-tête facultatif Windows-Specific champs (image uniquement)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Caractéristiques des DLL étendues

Les valeurs suivantes sont définies pour les bits de caractéristiques de la DLL étendue.

| Constante | Valeur | Description |
|-|-|-|
| IMAGE \_ DLLCHARACTERISTICS \_ ex \_ . \_ compatibilité | 0x0001 | L’image est compatible avec l’heure d’été. |

#### <a name="debugf-object-only"></a>. Debug $ F (objet uniquement)

Les données de cette section ont été remplacées dans Visual C++ version 7,0 et les versions ultérieures par un ensemble plus complet de données émises dans une sous-section **$ S Debug** .

Les fichiers objets peuvent contenir des sections. Debug $ F dont le contenu est un ou plusieurs \_ enregistrements de données FPO (informations d’omission du pointeur de frame). Consultez « IMAGE \_ Debug \_ type \_ FPO » dans [type de débogage](#debug-type).

L’éditeur de liens reconnaît ces enregistrements **. Debug $ F** . Si des informations de débogage sont générées, l’éditeur de liens trie les \_ enregistrements de données FPO par RVA de procédure et génère une entrée de répertoire de débogage pour eux.

Le compilateur ne doit pas générer d’enregistrements FPO pour les procédures qui ont un format de cadre standard.

#### <a name="debugs-object-only"></a>. déboguer $ S (objet uniquement)

Cette section contient Visual C++ informations de débogage (informations symboliques).

#### <a name="debugp-object-only"></a>. Debug $ P (objet uniquement)

Cette section contient Visual C++ informations de débogage (informations précompilées). Il s’agit de types partagés parmi tous les objets qui ont été compilés à l’aide de l’en-tête précompilé qui a été généré avec cet objet.

#### <a name="debugt-object-only"></a>. Debug $ T (objet uniquement)

Cette section contient Visual C++ informations de débogage (informations de type).

#### <a name="linker-support-for-microsoft-debug-information"></a>Prise en charge de l’éditeur de liens pour les informations de débogage Microsoft

Pour prendre en charge les informations de débogage, l’éditeur de liens :

-   Rassemble toutes les données de débogage pertinentes à partir des sections **. Debug $ F**, **Debug $ S**, **. Debug $ P** et **. Debug $ T** .

-   Traite ces données avec les informations de débogage générées par l’éditeur de liens dans le fichier PDB et crée une entrée de répertoire de débogage pour y faire référence.

### <a name="the-drectve-section-object-only"></a>Section. drectve (objet uniquement)

Une section est une section de directive si elle possède l' \_ \_ Indicateur SCN LNK \_ info défini dans l’en-tête de la section et a le nom de la section **. drectve** . L’éditeur de liens supprime une section **. drectve** après avoir traité les informations, donc la section n’apparaît pas dans le fichier image qui est lié.

Une section **. drectve** se compose d’une chaîne de texte qui peut être encodée au format ANSI ou UTF-8. Si le marqueur d’ordre d’octet UTF-8 (BOM, un préfixe de trois octets qui se compose de 0xEF, 0xBB et 0xBF) n’est pas présent, la chaîne de directive est interprétée comme ANSI. La chaîne de directive est une série d’options de l’éditeur de liens séparées par des espaces. Chaque option contient un trait d’Union, le nom de l’option et tout attribut approprié. Si une option contient des espaces, l’option doit être placée entre guillemets. La section **. drectve** ne doit pas avoir de réadressages ou de numéros de ligne.

### <a name="the-edata-section-image-only"></a>Section. edata (image uniquement)

La section Export Data, nommée. edata, contient des informations sur les symboles auxquels d’autres images peuvent accéder via la liaison dynamique. Les symboles exportés se trouvent généralement dans les dll, mais les dll peuvent également importer des symboles.

Une vue d’ensemble de la structure générale de la section exportation est décrite ci-dessous. Les tables décrites sont généralement contiguës dans le fichier dans l’ordre indiqué (bien que cela ne soit pas obligatoire). Seule la table d’exportation et la table d’adresses d’exportation sont requises pour exporter les symboles en tant qu’ordinaux. (Un ordinal est une exportation accessible directement par son index de table d’adresses d’exportation.) La table de pointeur de nom, la table ordinale et la table de noms d’exportation existent pour prendre en charge l’utilisation des noms d’exportation.



| Nom de la table                         | Description                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exporter une table de répertoire <br/> | Table avec une seule ligne (contrairement au répertoire de débogage). Ce tableau indique les emplacements et les tailles des autres tables d’exportation. <br/>                                                                                                                                                                                                               |
| Exporter une table d’adresses <br/>   | Tableau de RVA des symboles exportés. Il s’agit des adresses réelles des fonctions et des données exportées dans le code exécutable et les sections de données. D’autres fichiers images peuvent importer un symbole à l’aide d’un index de cette table (un ordinal) ou, éventuellement, en utilisant le nom public qui correspond à l’ordinal si un nom public est défini. <br/> |
| Nom de la table de pointeurs <br/>     | Tableau de pointeurs vers les noms d’exportation publics, triés dans l’ordre croissant. <br/>                                                                                                                                                                                                                                                                    |
| Table ordinale <br/>          | Tableau des ordinaux qui correspondent aux membres de la table de pointeurs de nom. La correspondance est par position ; par conséquent, la table de pointeurs de nom et la table ordinale doivent avoir le même nombre de membres. Chaque ordinal est un index dans la table d’adresses d’exportation. <br/>                                                                        |
| Exporter le nom table <br/>      | Une série de chaînes ASCII se terminant par un caractère null. Les membres de la table de pointeur de nom pointent dans cette zone. Ces noms sont les noms publics par le biais desquels les symboles sont importés et exportés ; ils ne sont pas nécessairement les mêmes que les noms privés utilisés dans le fichier image. <br/>                                                           |



 

Lorsqu’un autre fichier image importe un symbole par nom, le chargeur Win32 recherche une chaîne correspondante dans la table de pointeur de nom. Si une chaîne correspondante est trouvée, l’ordinal associé est identifié en recherchant le membre correspondant dans la table ordinale (autrement dit, le membre de la table ordinale avec le même index que le pointeur de chaîne trouvé dans la table de pointeur de nom). L’ordinal résultant est un index dans la table d’adresses d’exportation, qui donne l’emplacement réel du symbole souhaité. Chaque symbole d’exportation est accessible par un ordinal.

Lorsqu’un autre fichier image importe un symbole par ordinal, il n’est pas nécessaire d’effectuer une recherche dans la table de pointeur de nom pour une chaîne correspondante. L’utilisation directe d’un ordinal est donc plus efficace. Toutefois, un nom d’exportation est plus facile à mémoriser et ne demande pas à l’utilisateur de connaître l’index de table pour le symbole.

#### <a name="export-directory-table"></a>Exporter une table de répertoire

Les informations sur les symboles d’exportation commencent par la table de répertoire d’exportation, qui décrit le reste des informations de symbole d’exportation. La table exporter le répertoire contient des informations d’adresse utilisées pour résoudre les importations des points d’entrée dans cette image.



| Offset         | Taille          | Champ                                | Description                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Exporter les indicateurs <br/>             | Réservé, doit avoir la valeur 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Horodatage <br/>          | Heure et date de création des données d’exportation. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Version majeure <br/>            | Numéro de version principale. Les numéros de version majeure et mineure peuvent être définis par l’utilisateur. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Version mineure <br/>            | Numéro de version secondaire. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nom RVA <br/>                 | Adresse de la chaîne ASCII qui contient le nom de la DLL. Cette adresse est relative à la base de l’image. <br/>                                                |
| 16 <br/> | 4 <br/> | Base ordinale <br/>             | Nombre ordinal de départ pour les exportations dans cette image. Ce champ spécifie le numéro ordinal de début de la table d’adresses d’exportation. Il est généralement défini sur 1. <br/> |
| 20 <br/> | 4 <br/> | Entrées de la table Address <br/>    | Nombre d’entrées dans la table d’adresses d’exportation. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Nombre de pointeurs de nom <br/>  | Nombre d’entrées dans la table de pointeurs de nom. Il s’agit également du nombre d’entrées dans la table ordinale. <br/>                                                     |
| 28 <br/> | 4 <br/> | Adresse RVA d’exportation de table d’adresses <br/> | Adresse de la table d’adresses d’exportation, par rapport à la base de l’image. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | Nom RVA du pointeur de nom <br/>         | Adresse de la table de pointeurs du nom d’exportation, relative à la base de l’image. La taille de la table est donnée par le champ nombre de pointeurs de nom. <br/>                       |
| 36 <br/> | 4 <br/> | RVA de table ordinale <br/>        | Adresse de la table ordinale par rapport à la base de l’image. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Exporter une table d’adresses

La table d’adresses d’exportation contient l’adresse des points d’entrée exportés et des données exportées et des données absolues. Un nombre ordinal est utilisé comme index dans la table d’adresses d’exportation.

Chaque entrée dans la table d’adresses d’exportation est un champ qui utilise l’un des deux formats figurant dans le tableau suivant. Si l’adresse spécifiée n’est pas comprise dans la section d’exportation (comme défini par l’adresse et la longueur indiqués dans l’en-tête facultatif), le champ est un RVA d’exportation, qui est une adresse réelle dans le code ou les données. Dans le cas contraire, le champ est un RVA de redirecteur, qui nomme un symbole dans une autre DLL.



| Offset        | Taille          | Champ                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exporter un RVA <br/>    | Adresse du symbole exporté lorsqu’il est chargé en mémoire, par rapport à la base de l’image. Par exemple, l’adresse d’une fonction exportée. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | RVA du redirecteur <br/> | Pointeur vers une chaîne ASCII terminée par le caractère NULL dans la section d’exportation. Cette chaîne doit être comprise dans la plage fournie par l’entrée de répertoire de données de table d’exportation. Consultez les [répertoires de données d’en-tête facultatifs (image uniquement)](#optional-header-data-directories-image-only). Cette chaîne indique le nom de la DLL et le nom de l’exportation (par exemple, « MYDLL. expfunc ») ou le nom de la DLL et le numéro ordinal de l’exportation (par exemple, «MYDLL. \# 27 "). <br/> |



 

Une adresse RVA de redirecteur exporte une définition à partir d’une autre image, en la faisant apparaître comme si elle était exportée par l’image actuelle. Par conséquent, le symbole est importé et exporté simultanément.

par exemple, dans Kernel32.dll dans Windows XP, l’exportation nommée « HeapAlloc » est transmise à la chaîne «NTDLL. RtlAllocateHeap." cela permet aux applications d’utiliser le Ntdll.dll de module spécifique à Windows XP sans réellement contenir des références d’importation. La table d’importation de l’application fait uniquement référence à Kernel32.dll. par conséquent, l’application n’est pas spécifique à Windows XP et peut s’exécuter sur n’importe quel système Win32.

#### <a name="export-name-pointer-table"></a>Exporter le nom de la table de pointeurs

La table de pointeurs de nom d’exportation est un tableau d’adresses (RVA) dans la table de noms d’exportation. Les pointeurs sont 32 bits chacun et sont relatifs à la base de l’image. Les pointeurs sont triés lexicalement pour autoriser les recherches binaires.

Un nom d’exportation est défini uniquement si la table du pointeur de nom d’exportation contient un pointeur vers celui-ci.

#### <a name="export-ordinal-table"></a>Exporter une table ordinale

La table ordinale d’exportation est un tableau d’index non biaisés 16 bits dans la table d’adresses d’exportation. Les ordinaux sont faussés par le champ de base ordinal de la table de répertoire d’exportation. En d’autres termes, la base ordinale doit être soustraite des ordinaux pour obtenir les véritables index dans la table d’adresses d’exportation.

La table du pointeur de nom d’exportation et la table ordinale d’exportation forment deux tableaux parallèles séparés pour permettre l’alignement de champ naturel. Ces deux tables, en effet, fonctionnent comme une seule table, dans laquelle la colonne de pointeur de nom d’exportation pointe vers un nom public (exporté) et la colonne d’ordinal d’exportation donne l’ordinal correspondant pour ce nom public. Un membre de la table de pointeurs de nom d’exportation et un membre de la table ordinale d’exportation sont associés à la même position (index) dans leurs tableaux respectifs.

Ainsi, lorsque la table de pointeurs de nom d’exportation est recherchée et qu’une chaîne correspondante est trouvée à la position i, l’algorithme de recherche des RVA du symbole et de l’ordinal biaisé est le suivant :

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Lors de la recherche d’un symbole (biais) ordinal, l’algorithme permettant de trouver l’adresse RVA du symbole et le nom est :

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Exporter le nom table

La table nom d’exportation contient les données de chaîne réelles pointées par la table du pointeur de nom d’exportation. Les chaînes de cette table sont des noms publics que d’autres images peuvent utiliser pour importer les symboles. Ces noms d’exportation publics ne sont pas nécessairement les mêmes que les noms de symboles privés dont disposent les symboles dans leur propre fichier image et code source, bien qu’ils puissent l’être.

Chaque symbole exporté a une valeur ordinale, qui est simplement l’index dans la table d’adresses d’exportation. Toutefois, l’utilisation de noms d’exportation est facultative. Tout, tout ou aucun des symboles exportés peut avoir des noms d’exportation. Pour les symboles exportés qui ont des noms d’exportation, les entrées correspondantes dans la table de pointeur de nom d’exportation et la table ordinale d’exportation fonctionnent ensemble pour associer chaque nom à un ordinal.

La structure de la table de noms d’exportation est une série de chaînes ASCII se terminant par un caractère null de longueur variable.

### <a name="the-idata-section"></a>Section. idata

Tous les fichiers image qui importent des symboles, y compris pratiquement tous les fichiers exécutables (EXE), ont une section. idata. Une mise en page de fichier standard pour les informations d’importation est la suivante :

-   Table de répertoire

    Entrée de répertoire null

-   DLL1 importer la table de recherche

    Null

-   DLL2 importer la table de recherche

    Null

-   DLL3 importer la table de recherche

    Null

-   Table Hint-Name

#### <a name="import-directory-table"></a>Importer une table de répertoire

Les informations d’importation commencent par la table d’importation des répertoires, qui décrit le reste des informations d’importation. La table du répertoire d’importation contient des informations d’adresse utilisées pour résoudre les références de correction aux points d’entrée dans une image DLL. La table d’importation des répertoires se compose d’un tableau d’entrées de répertoire d’importation, d’une entrée pour chaque DLL à laquelle l’image fait référence. La dernière entrée de répertoire est vide (remplie avec des valeurs null), ce qui indique la fin de la table de répertoires.

Chaque entrée de répertoire d’importation a le format suivant :



| Offset         | Taille          | Champ                                                 | Description                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importer les RVA de table de recherche (caractéristiques) <br/> | Adresse RVA de la table de recherche d’importation. Cette table contient un nom ou un ordinal pour chaque importation. (Le nom « caractéristiques » est utilisé dans Winnt. h, mais ne décrit plus ce champ.) <br/> |
| 4 <br/>  | 4 <br/> | Horodatage <br/>                           | Horodatage défini à zéro jusqu’à ce que l’image soit liée. Une fois l’image liée, ce champ a pour valeur l’horodatage de la DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Chaîne de redirecteur <br/>                           | Index de la première référence de redirecteur. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nom RVA <br/>                                  | Adresse d’une chaîne ASCII qui contient le nom de la DLL. Cette adresse est relative à la base de l’image. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importer une adresse RVA de table d’adresses (table thunk) <br/>    | Adresse RVA de la table d’adresses d’importation. Le contenu de cette table est identique au contenu de la table de recherche d’importation jusqu’à ce que l’image soit liée. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importer une table de recherche

Une table de recherche d’importation est un tableau de nombres 32 bits pour PE32 ou un tableau de nombres 64 bits pour PE32 +. Chaque entrée utilise le format de champ de bits qui est décrit dans le tableau suivant. Dans ce format, le bit 31 est le bit le plus significatif pour PE32 et le bit 63 est le bit le plus significatif pour PE32 +. La collection de ces entrées décrit toutes les importations à partir d’une DLL donnée. La dernière entrée est définie sur zéro (NULL) pour indiquer la fin de la table.



| Bit(s)            | Taille           | Champ de bits                       | Description                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Indicateur de nom/ordinal <br/>   | Si ce bit est défini, importez par ordinal. Dans le cas contraire, importez par nom. Le bit est masqué en 0x80000000 pour PE32, 0x8000000000000000 pour PE32 +. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Nombre ordinal <br/>      | Nombre ordinal de 16 bits. Ce champ est utilisé uniquement si le champ de bits de l’indicateur ordinal/nom est 1 (importer par ordinal). Les bits 30-15 ou 62-15 doivent avoir la valeur 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | Adresse RVA/nom de la table RVA <br/> | RVA de 31 bits d’une entrée de table Hint/Name. Ce champ est utilisé uniquement si le champ de bits de l’indicateur ordinal/nom a la valeur 0 (importer par nom). Pour PE32 + bits 62-31 doit être égal à zéro. <br/> |



 

#### <a name="hintname-table"></a>Table Hint/Name

Une table Hint/Name est suffisante pour l’intégralité de la section Import. Chaque entrée dans la table Hint/Name a le format suivant :



| Offset         | Taille                 | Champ            | Description                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Évit <br/> | Index dans la table de pointeurs de nom d’exportation. Une correspondance est tentée en premier avec cette valeur. En cas d’échec, une recherche binaire est effectuée sur la table du pointeur de nom d’exportation de la DLL. <br/>            |
| 2 <br/>  | variable <br/> | Name <br/> | Chaîne ASCII qui contient le nom à importer. Il s’agit de la chaîne qui doit être mise en correspondance avec le nom public dans la DLL. Cette chaîne respecte la casse et se termine par un octet NULL. <br/> |
| \* <br/> | 0 ou 1 <br/>   | Remplir <br/>  | Octet de remplissage zéro à droite qui apparaît après l’octet NULL de fin, si nécessaire, pour aligner l’entrée suivante sur une limite égale. <br/>                                                        |



 

#### <a name="import-address-table"></a>Table d’adresses d’importation

La structure et le contenu de la table d’adresses d’importation sont identiques à ceux de la table de recherche d’importation, jusqu’à ce que le fichier soit lié. Pendant la liaison, les entrées de la table d’adresses d’importation sont remplacées par les adresses 32 bits (pour PE32) ou 64 bits (pour PE32 +) des symboles en cours d’importation. Ces adresses sont les adresses mémoire réelles des symboles, bien qu’elles soient techniquement appelées « adresses virtuelles ». Le chargeur traite généralement la liaison.

### <a name="the-pdata-section"></a>La section. pdata

La section. pData contient un tableau d’entrées de table de fonctions utilisées pour la gestion des exceptions. Elle est référencée par l’entrée de la table d’exceptions dans le répertoire de données de l’image. Les entrées doivent être triées en fonction des adresses des fonctions (le premier champ de chaque structure) avant d’être émises dans l’image finale. La plateforme cible détermine laquelle des trois variantes de format d’entrée de table de fonction décrites ci-dessous est utilisée.

Pour les images MIPS 32 bits, les entrées de la table de fonctions ont le format suivant :



| Offset         | Taille          | Champ                          | Description                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Adresse de début <br/>      | VA de la fonction correspondante. <br/>                              |
| 4 <br/>  | 4 <br/> | Adresse de fin <br/>        | VA de la fin de la fonction. <br/>                                 |
| 8 <br/>  | 4 <br/> | Gestionnaire d’exceptions <br/>  | Pointeur vers le gestionnaire d’exceptions à exécuter. <br/>               |
| 12 <br/> | 4 <br/> | Données du gestionnaire <br/>       | Pointeur vers des informations supplémentaires à passer au gestionnaire. <br/> |
| 16 <br/> | 4 <br/> | Adresse de fin du prologue <br/> | VA de la fin du prologue de la fonction. <br/>                        |



 

pour les plateformes ARM, PowerPC, SH3 et SH4 Windows CE, les entrées de la table de fonctions ont le format suivant :



| Offset        | Taille                | Champ                       | Description                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Adresse de début <br/>   | VA de la fonction correspondante. <br/>                                                                         |
| 4 <br/> | 8 bits <br/>  | Longueur du prologue <br/>   | Nombre d’instructions dans le prologue de la fonction. <br/>                                                          |
| 4 <br/> | 22 bits <br/> | Longueur de la fonction <br/> | Nombre d’instructions dans la fonction. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Indicateur 32 bits <br/>     | Si cette valeur est définie, la fonction se compose d’instructions 32 bits. Si elle est désactivée, la fonction se compose d’instructions 16 bits. <br/> |
| 4 <br/> | 1 bit <br/>   | Indicateur d’exception <br/>  | S’il est défini, il existe un gestionnaire d’exceptions pour la fonction. Sinon, il n’existe aucun gestionnaire d’exceptions. <br/>                 |



 

Pour les plateformes x64 et Itanium, les entrées de table de fonctions ont le format suivant :



| Offset        | Taille          | Champ                          | Description                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Adresse de début <br/>      | RVA de la fonction correspondante. <br/> |
| 4 <br/> | 4 <br/> | Adresse de fin <br/>        | RVA de la fin de la fonction. <br/>    |
| 8 <br/> | 4 <br/> | Informations de déroulement <br/> | Adresse RVA des informations de déroulement. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Section. reloc (image uniquement)

La table de réadressage de base contient des entrées pour toutes les réadressages de base dans l’image. Le champ de table de réadressage de base dans les répertoires de données d’en-tête facultatifs indique le nombre d’octets dans la table de réadressage de base. Pour plus d’informations, consultez [répertoires de données d’en-tête facultatifs (image uniquement)](#optional-header-data-directories-image-only). La table de réadressage de base est divisée en blocs. Chaque bloc représente les réadressages de base pour une page 4K. Chaque bloc doit démarrer sur une limite de 32 bits.

Le chargeur n’est pas requis pour traiter les réadressages de base résolus par l’éditeur de liens, sauf si l’image de chargement ne peut pas être chargée au niveau de la base d’image spécifiée dans l’en-tête PE.

#### <a name="base-relocation-block"></a>Bloc de réadressage de base

Chaque bloc de réadressage de base commence par la structure suivante :



| Offset        | Taille          | Champ                  | Description                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | RVA de page <br/>   | La base de l’image plus l’adresse RVA de la page est ajoutée à chaque décalage pour créer le VA où le réadressage de base doit être appliqué. <br/>                         |
| 4 <br/> | 4 <br/> | Taille de bloc <br/> | Nombre total d’octets dans le bloc de réadressage de base, y compris les champs de la page RVA et de la taille de bloc, ainsi que les champs de type/décalage qui suivent. <br/> |



 

Le champ Taille de bloc est alors suivi de n’importe quel nombre d’entrées de champ de type ou de décalage. Chaque entrée est un mot (2 octets) et sa structure est la suivante :



| Offset        | Taille                | Champ              | Description                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bits <br/>  | Type <br/>   | Stocké dans les 4 bits de poids fort du mot, valeur qui indique le type de réadressage de base à appliquer. Pour plus d’informations, consultez [types de réadressage de base](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bits <br/> | Offset <br/> | Stocké dans les 12 bits restants du mot, décalage par rapport à l’adresse de départ spécifiée dans le champ de la page RVA du bloc. Ce décalage spécifie où le réadressage de base doit être appliqué. <br/> |



 

Pour appliquer un réadressage de base, la différence est calculée entre l’adresse de base préférée et la base dans laquelle l’image est réellement chargée. Si l’image est chargée à sa base par défaut, la différence est égale à zéro et les réadressages de base ne doivent donc pas être appliqués.

#### <a name="base-relocation-types"></a>Types de réadressage de base



| Constante                                       | Valeur          | Description                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ \_ basée sur une rel. \_ <br/>        | 0 <br/>  | Le réadressage de base est ignoré. Ce type peut être utilisé pour remplir un bloc. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ basée sur la \_ hauteur <br/>            | 1 <br/>  | Le réadressage de base ajoute les 16 bits de poids fort de la différence au champ de 16 bits au décalage. Le champ de 16 bits représente la valeur élevée d’un mot de 32 bits. <br/>                                                                                                                                                               |
| base d’IMAGE \_ rel \_ \_ faible <br/>             | 2 <br/>  | Le réadressage de base ajoute les 16 bits de poids faible de la différence au champ de 16 bits au décalage. Le champ de 16 bits représente la moitié inférieure d’un mot de 32 bits. <br/>                                                                                                                                                                  |
| \_ \_ HIGHLOW basé sur une image \_ <br/>         | 3 <br/>  | Le réadressage de base applique tous les 32 bits de la différence au champ de 32 bits au décalage. <br/>                                                                                                                                                                                                                              |
| \_ \_ HIGHADJ basé sur une image \_ <br/>         | 4 <br/>  | Le réadressage de base ajoute les 16 bits de poids fort de la différence au champ de 16 bits au décalage. Le champ de 16 bits représente la valeur élevée d’un mot de 32 bits. Les 16 bits de poids faible de la valeur 32 bits sont stockés dans le mot 16 bits qui suit ce réadressage de base. Cela signifie que ce réadressage de base occupe deux emplacements. <br/> |
| \_JMPADDR des \_ mips basés sur une \_ image \_ <br/>   | 5 <br/>  | L’interprétation du réadressage dépend du type d’ordinateur. <br/> Lorsque le type d’ordinateur est MIPS, le réadressage de base s’applique à une instruction de saut MIPS. <br/>                                                                                                                                                    |
| IMAGE \_ \_ MOV32 ARM basé sur une rel. \_ \_ <br/>      | 5 <br/>  | Ce déplacement est significatif uniquement lorsque le type d’ordinateur est ARM ou Thumb. Le réadressage de base applique l’adresse 32 bits d’un symbole sur une paire d’instructions MOVW/MOVT consécutive. <br/>                                                                                                                                 |
| \_ \_ \_ RISCV HIGH20 basé sur \_ une image <br/>   | 5 <br/>  | Ce déplacement est significatif uniquement lorsque le type d’ordinateur est RISC-V. Le réadressage de base s’applique aux 20 bits de poids fort d’une adresse absolue de 32 bits. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Réservé, doit être égal à zéro. <br/>                                                                                                                                                                                                                                                                                               |
| \_ \_ \_ MOV32 Thumb basé sur \_ une image rel <br/>    | 7 <br/>  | Ce déplacement est significatif uniquement lorsque le type d’ordinateur est Thumb. Le réadressage de base applique l’adresse 32 bits d’un symbole à une paire d’instructions MOVW/MOVT consécutive. <br/>                                                                                                                                            |
| \_ \_ \_ RISCV LOW12I basé sur \_ une image <br/>   | 7 <br/>  | Ce déplacement est significatif uniquement lorsque le type d’ordinateur est RISC-V. Le réadressage de base s’applique aux 12 bits de poids faible d’une adresse absolue 32 bits formée dans le format d’instruction de type I RISC-V. <br/>                                                                                                                           |
| \_ \_ \_ RISCV LOW12S basé sur \_ une image <br/>   | 8 <br/>  | Ce déplacement est significatif uniquement lorsque le type d’ordinateur est RISC-V. Le réadressage de base s’applique aux 12 bits de poids faible d’une adresse absolue de 32 bits formée dans le format d’instruction de type S RISC-V. <br/>                                                                                                                           |
| \_JMPADDR16 des \_ mips basés sur une \_ image \_ <br/> | 9 <br/>  | Le déplacement est significatif uniquement lorsque le type d’ordinateur est MIPS. Le réadressage de base s’applique à une instruction de saut MIPS16. <br/>                                                                                                                                                                                            |
| \_ \_ DIR64 basé sur une image \_ <br/>           | 10 <br/> | Le réadressage de base applique la différence au champ de bits 64 au décalage. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>Section. TLS

La section. TLS fournit la prise en charge directe de PE et de COFF pour le stockage local des threads (TLS) statique. TLS est une classe de stockage spéciale que Windows prend en charge, dans laquelle un objet de données n’est pas une variable automatique (pile), mais est local pour chaque thread qui exécute le code. Ainsi, chaque thread peut conserver une valeur différente pour une variable déclarée à l’aide de TLS.

Notez que toute quantité de données TLS peut être prise en charge à l’aide des appels d’API TlsAlloc, TlsFree, TlsSetValue et TlsGetValue. L’implémentation PE ou COFF est une approche alternative à l’utilisation de l’API et présente l’avantage d’être plus simple du point de vue du programmeur de langage de haut niveau. Cette implémentation permet de définir et d’initialiser les données TLS de la même façon que les variables statiques ordinaires dans un programme. par exemple, dans Visual C++, une variable TLS statique peut être définie comme suit, sans utiliser l’API Windows :

`__declspec (thread) int tlsFlag = 1;`

Pour prendre en charge cette construction de programmation, la section PE et COFF. TLS spécifie les informations suivantes : les données d’initialisation, les routines de rappel pour l’initialisation et l’arrêt par thread, et l’index TLS, qui sont expliqués dans la discussion suivante.

> [!Note]
>
> Les objets de données TLS déclarés statiquement peuvent être utilisés uniquement dans des fichiers image chargés statiquement. En effet, il n’est pas fiable d’utiliser des données TLS statiques dans une DLL, sauf si vous savez que la DLL, ou quelque chose qui lui est lié de manière statique, ne sera jamais chargée de manière dynamique avec la fonction de l’API LoadLibrary.

 

Le code exécutable accède à un objet de données TLS statique en procédant comme suit :

1.  Au moment de la liaison, l’éditeur de liens définit l’adresse du champ d’index du répertoire TLS. Ce champ pointe vers un emplacement où le programme s’attend à recevoir l’index TLS.

    La bibliothèque Runtime de Microsoft facilite ce processus en définissant une image mémoire du répertoire TLS et en lui attribuant le nom spécial « \_ \_ TLS \_ utilisé » (plates-formes Intel x86) ou « \_ TLS \_ utilisé » (autres plateformes). L’éditeur de liens recherche cette image mémoire et y utilise les données pour créer le répertoire TLS. Les autres compilateurs qui prennent en charge TLS et qui fonctionnent avec l’éditeur de liens Microsoft doivent utiliser cette même technique.

2.  Quand un thread est créé, le chargeur communique l’adresse du tableau TLS du thread en plaçant l’adresse du bloc d’environnement de thread (TEB) dans le registre FS. Un pointeur vers le tableau TLS se trouve au décalage de 0x2C à partir du début de TEB. Ce comportement est spécifique à Intel x86.

3.  Le chargeur affecte la valeur de l’index TLS à l’emplacement indiqué par l’adresse du champ d’index.

4.  Le code exécutable récupère l’index TLS et également l’emplacement du tableau TLS.

5.  Le code utilise l’index TLS et l’emplacement du tableau TLS (en multipliant l’index par 4 et en l’utilisant comme décalage du tableau) pour obtenir l’adresse de la zone de données TLS pour le programme et le module donnés. Chaque thread possède sa propre zone de données TLS, mais cela est transparent pour le programme, ce qui n’a pas besoin de savoir comment les données sont allouées pour des threads individuels.

6.  Un objet de données TLS individuel est accessible en tant qu’offset fixe dans la zone de données TLS.

Le tableau TLS est un tableau d’adresses géré par le système pour chaque thread. Chaque adresse de ce tableau indique l’emplacement des données TLS pour un module donné (EXE ou DLL) dans le programme. L’index TLS indique le membre du groupe à utiliser. L’index est un nombre (significatif uniquement pour le système) qui identifie le module.

#### <a name="the-tls-directory"></a>Le répertoire TLS

Le répertoire TLS a le format suivant :



| Décalage (PE32/PE32 +) | Taille (PE32/PE32 +) | Champ                            | Description                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | VA démarrer les données brutes <br/>    | Adresse de départ du modèle TLS. Le modèle est un bloc de données utilisé pour initialiser les données TLS. Le système copie toutes ces données chaque fois qu’un thread est créé, donc il ne doit pas être endommagé. Notez que cette adresse n’est pas un RVA. Il s’agit d’une adresse pour laquelle il doit y avoir un réadressage de base dans la section. reloc. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Fin des données brutes <br/>      | Adresse du dernier octet du TLS, à l’exception du remplissage zéro. Comme avec le champ de VA de début des données brutes, il s’agit d’un VA, et non d’un RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Adresse de l’index <br/>     | Emplacement de réception de l’index TLS que le chargeur affecte. Cet emplacement se trouve dans une section de données ordinaire et peut donc recevoir un nom symbolique accessible au programme. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Adresse des rappels <br/> | Pointeur vers un tableau de fonctions de rappel TLS. Le tableau se termine par un caractère NULL ; par conséquent, si aucune fonction de rappel n’est prise en charge, ce champ pointe vers la valeur zéro pour 4 octets. Pour plus d’informations sur le prototype de ces fonctions, consultez [fonctions de rappel TLS](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Taille de remplissage zéro <br/>    | Taille en octets du modèle, au-delà des données initialisées, délimitées par les champs de début et de fin des données brutes. La taille totale du modèle doit être identique à la taille totale des données TLS dans le fichier image. Le remplissage zéro correspond à la quantité de données qui vient après les données non null initialisées. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Caractéristiques <br/>      | Les quatre bits \[ 23:20 \] décrivent les informations d’alignement. Les valeurs possibles sont celles définies comme IMAGE \_ SCN \_ align \_ \* , qui sont également utilisées pour décrire l’alignement de la section dans les fichiers objets. Les 28 autres bits sont réservés pour une utilisation ultérieure. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Fonctions de rappel TLS

Le programme peut fournir une ou plusieurs fonctions de rappel TLS pour prendre en charge l’initialisation et l’arrêt supplémentaires pour les objets de données TLS. Une utilisation classique pour une telle fonction de rappel consisterait à appeler des constructeurs et des destructeurs pour les objets.

Bien qu’il n’y ait généralement pas plus d’une fonction de rappel, un rappel est implémenté en tant que tableau pour permettre l’ajout de fonctions de rappel supplémentaires si vous le souhaitez. S’il existe plusieurs fonctions de rappel, chaque fonction est appelée dans l’ordre dans lequel son adresse apparaît dans le tableau. Un pointeur null termine le tableau. Il est tout à fait possible d’avoir une liste vide (aucun rappel pris en charge), auquel cas le tableau de rappel a un seul membre, un pointeur null.

Le prototype d’une fonction de rappel (pointée par un pointeur de type PIMAGE \_ TLS \_ callback) a les mêmes paramètres qu’une fonction de point d’entrée dll :


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



Le paramètre réservé doit être défini à zéro. Le paramètre Reason peut prendre les valeurs suivantes :



| Paramètre                          | Valeur         | Description                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| \_attachement du processus dll \_ <br/> | 1 <br/> | Un nouveau processus a démarré, y compris le premier thread. <br/>                                   |
| \_attachement de thread dll \_ <br/>  | 2 <br/> | Un nouveau thread a été créé. Cette notification est envoyée pour tous les threads à l’exception du premier. <br/>      |
| \_détachement de thread dll \_ <br/>  | 3 <br/> | Un thread va être arrêté. Cette notification est envoyée pour tous les threads à l’exception du premier. <br/> |
| \_détachement de processus dll \_ <br/> | 0 <br/> | Un processus va se terminer, y compris le thread d’origine. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Structure de la configuration de charge (image uniquement)

La structure de la configuration de charge (répertoire de configuration \_ \_ de chargement d’image \_ ) était précédemment utilisée dans des cas très limités dans le système d’exploitation Windows NT lui-même pour décrire les différentes fonctionnalités trop difficiles ou trop grandes pour être décrites dans l’en-tête de fichier ou l’en-tête facultatif de l’image. les versions actuelles de Microsoft linker et Windows XP et les versions ultérieures de Windows utilisent une nouvelle version de cette structure pour les systèmes x86 32 bits qui incluent la technologie SEH réservée. Fournit la liste des gestionnaires d’exceptions structurés sécurisés que le système d’exploitation utilise pendant la distribution des exceptions. Si l’adresse du gestionnaire réside dans la plage de VA d’une image et si elle est marquée comme étant réservée à la gestion de la gestion des exceptions (autrement dit, l’IMAGE \_ DLLCHARACTERISTICS \_ non \_ SEH n’est pas claire dans le champ DLLCHARACTERISTICS de l’en-tête facultatif, comme décrit précédemment), le gestionnaire doit figurer dans la liste des gestionnaires sécurisés connus pour cette image. Dans le cas contraire, le système d’exploitation met fin à l’application. Cela permet d’éviter l’exploit « détournement du gestionnaire d’exceptions x86 » qui a été utilisé par le passé pour prendre le contrôle du système d’exploitation.

L’éditeur de liens de Microsoft fournit automatiquement une structure de configuration de charge par défaut pour inclure les données SEH réservées. Si le code utilisateur fournit déjà une structure de configuration de charge, il doit inclure les nouveaux champs SEH réservés. Dans le cas contraire, l’éditeur de liens ne peut pas inclure les données SEH réservées et l’image n’est pas marquée comme contenant la fonction SEH réservée.

#### <a name="load-configuration-directory"></a>Charger le répertoire de configuration

L’entrée de répertoire de données pour une structure de configuration de chargement SEH préréservée doit spécifier une taille particulière de la structure de la configuration de charge, car le chargeur du système d’exploitation s’attend toujours à une certaine valeur. À cet égard, la taille est véritablement uniquement une vérification de version. pour la compatibilité avec Windows XP et les versions antérieures de Windows, la taille doit être de 64 pour les images x86.

#### <a name="load-configuration-layout"></a>Charger la disposition de configuration

La structure de la configuration de chargement présente la disposition suivante pour les fichiers PE 32 bits et 64 bits :



| Offset              | Taille            | Champ                                      | Description                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Caractéristiques <br/>                | Indicateurs qui indiquent les attributs du fichier, actuellement inutilisés. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valeur d’horodatage de date et d’heure. La valeur est représentée dans le nombre de secondes qui se sont écoulées depuis minuit (00:00:00), le 1er janvier 1970, heure UTC (Universal Coordinated Time), en fonction de l’horloge système. L’horodatage peut être imprimé à l’aide de la fonction Time du runtime C (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Numéro de version principale. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Numéro de version secondaire. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Indicateur de chargeur global à effacer pour ce processus lorsque le chargeur démarre le processus. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Indicateurs de chargeur global à définir pour ce processus lorsque le chargeur démarre le processus. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Valeur de délai d’attente par défaut à utiliser pour les sections critiques de ce processus qui sont abandonnées. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Mémoire qui doit être libérée avant d’être retournée au système, en octets. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Quantité totale de mémoire disponible, en octets. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 uniquement \] la va d’une liste d’adresses où le préfixe de verrouillage est utilisé afin de pouvoir être remplacé par NOP sur les ordinateurs à un seul processeur. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Taille d’allocation maximale, en octets. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Taille maximale de la mémoire virtuelle, en octets. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | La définition de ce champ sur une valeur différente de zéro équivaut à appeler SetProcessAffinityMask avec cette valeur lors du démarrage du processus (.exe uniquement) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Traitez les indicateurs de tas qui correspondent au premier argument de la fonction HeapCreate. Ces indicateurs s’appliquent au tas de processus créé lors du démarrage du processus. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Identificateur de la version du Service Pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Réservé <br/>                       | Doit être zéro. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | EditList <br/>                       | Réservé à une utilisation par le système. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Pointeur vers un cookie utilisé par Visual C++ ou l’implémentation GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 uniquement \] la VA de la table triée des adresses rva de chaque gestionnaire de SE valides et uniques dans l’image. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[x86 uniquement \] le nombre de gestionnaires uniques dans la table. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | VA où le pointeur de la fonction de contrôle Flow Guard est stocké. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | l’emplacement de stockage du pointeur de fonction de contrôle Flow Guard. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | la VA de la table triée des adresses rva de chaque contrôle Flow fonction Guard dans l’image. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | Nombre d’adresses RVA uniques dans la table ci-dessus. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | contrôle Flow les indicateurs liés à Guard. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Informations d’intégrité du code. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | l’emplacement de stockage de la table IAT de l’adresse de contrôle Flow Guard est stocké. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | Nombre d’adresses RVA uniques dans la table ci-dessus. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | l’emplacement de stockage de la table cible de saut long de contrôle Flow Guard. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | Nombre d’adresses RVA uniques dans la table ci-dessus. <br/>                                                                                                                                                                                                                                    |



 

Le champ GuardFlags contient une combinaison d’un ou plusieurs des indicateurs et sous-champs suivants :

-   Module effectue des vérifications de l’intégrité du workflow à l’aide de la prise en charge fournie par le système.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   Le module effectue des contrôles de workflow et d’intégrité en écriture.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   Le module contient des métadonnées cibles de workflow de contrôle valides.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   Le module n’utilise pas le cookie de sécurité/GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   Le module prend en charge l’IAT de chargement différé en lecture seule.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   DELAYLOAD Import table dans sa propre section. didat (avec rien d’autre) qui peut être reprotégé librement.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   Le module contient des informations d’exportation supprimées. Cela déduit également que la table IAT Address comprise est également présente dans la configuration de chargement.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   Le module permet la suppression des exportations.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   Le module contient des informations sur la cible longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   masque pour le sous-champ qui contient le stride des entrées de la table de fonctions de contrôle Flow Guard (autrement dit, le nombre supplémentaire d’octets par entrée de table).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

en outre, l’SDK Windows en-tête winnt. h définit cette macro pour le nombre de bits de décalage vers la droite de la valeur GuardFlags pour justifier à droite le tableau de la fonction de contrôle Flow Guard :

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Section. rsrc

Les ressources sont indexées par une structure d’arborescence triée binaire à plusieurs niveaux. La conception générale peut incorporer 2 \* \* 31 niveaux. par convention, toutefois, Windows utilise trois niveaux :

<dl> Type  
Nom  
Langage  
</dl>

Une série de tables de répertoires de ressources relient tous les niveaux de la manière suivante : chaque table de répertoires est suivie d’une série d’entrées de répertoire qui fournissent le nom ou l’identificateur (ID) de ce niveau (type, nom ou niveau de langage) et une adresse de description de données ou une autre table de répertoire. Si l’adresse pointe vers une description de données, les données sont une feuille dans l’arborescence. Si l’adresse pointe vers une autre table de répertoire, cette table répertorie les entrées de répertoire au niveau supérieur suivant.

Les ID de type, de nom et de langue d’une feuille sont déterminés par le chemin d’accès utilisé par les tables de répertoires pour atteindre la feuille. La première table détermine l’ID de type, la deuxième table (désignée par l’entrée de répertoire de la première table), et la troisième table détermine l’ID de langue.

La structure générale de la section. rsrc est la suivante :



| Données                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tables de répertoires de ressources (et entrées de répertoire de ressources) <br/> | Une série de tables, une pour chaque groupe de nœuds dans l’arborescence. Tous les nœuds de niveau supérieur (type) sont répertoriés dans le premier tableau. Les entrées de ce tableau pointent vers les tables de second niveau. Chaque arborescence de second niveau a le même ID de type mais des ID de noms différents. Les arborescences de troisième niveau ont les mêmes ID de type et de nom, mais des ID de langue différents. <br/> Chaque table individuelle est immédiatement suivie d’entrées de répertoire, dans lesquelles chaque entrée a un nom ou un identificateur numérique et un pointeur vers une description de données ou une table au niveau inférieur suivant. <br/> |
| Chaînes de répertoire de ressources <br/>                                 | Chaînes Unicode alignées sur deux octets, qui servent de données de chaîne pointées par des entrées de répertoire. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Description des données de ressource <br/>                                  | Tableau d’enregistrements, désigné par des tables, qui décrivent la taille et l’emplacement réels des données de ressource. Ces enregistrements sont les feuilles de l’arborescence de la description des ressources. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Données de ressource <br/>                                              | Données brutes de la section de la ressource. Les informations relatives à la taille et à l’emplacement dans le champ descriptions des données de ressource délimitent les régions individuelles des données de ressource. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Table de répertoire des ressources

Chaque table de répertoire de ressources a le format suivant. Cette structure de données doit être considérée comme l’en-tête d’une table, car la table se compose en fait d’entrées de répertoire (décrites dans la section 6.9.2, « entrées de répertoire de ressources ») et de cette structure :



| Offset         | Taille          | Champ                              | Description                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caractéristiques <br/>        | Indicateurs de ressource. Ce champ est réservé à une utilisation ultérieure. Il est actuellement défini à zéro. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Horodatage <br/>        | Heure à laquelle les données de ressource ont été créées par le compilateur de ressources. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Version majeure <br/>          | Numéro de version principale, défini par l’utilisateur. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Version mineure <br/>          | Numéro de version secondaire, défini par l’utilisateur. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Nombre d’entrées de nom <br/> | Nombre d’entrées de répertoire qui suivent immédiatement la table qui utilise des chaînes pour identifier les entrées de type, de nom ou de langue (selon le niveau de la table). <br/> |
| 14 <br/> | 2 <br/> | Nombre d’entrées d’ID <br/>   | Nombre d’entrées de répertoire qui suivent immédiatement les entrées de nom qui utilisent des ID numériques pour les entrées de type, de nom ou de langue. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Entrées de répertoire de ressources

Les entrées d’annuaire composent les lignes d’une table. Chaque entrée de répertoire de ressources a le format suivant. Le fait que l’entrée soit un nom ou une entrée d’ID est indiqué par la table de répertoire de ressources, qui indique le nombre d’entrées de nom et d’ID suivies (souvenez-vous que toutes les entrées de nom précèdent toutes les entrées d’ID de la table). Toutes les entrées de la table sont triées dans l’ordre croissant : les entrées de nom par chaîne respectant la casse et les entrées d’ID par valeur numérique. Les décalages sont relatifs à l’adresse dans la \_ ressource d’entrée de répertoire d’images \_ \_ DataDirectory. Pour plus d’informations, consultez [homologation dans le PE : visite guidée du format de fichier exécutable portable Win32](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) .



| Offset        | Taille          | Champ                           | Description                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Décalage du nom <br/>         | Offset d’une chaîne qui donne le type, le nom ou l’entrée d’ID de langue, en fonction du niveau de la table. <br/>     |
| 0 <br/> | 4 <br/> | ID entier <br/>          | Entier 32 bits qui identifie le type, le nom ou l’entrée de l’ID de langue. <br/>                                   |
| 4 <br/> | 4 <br/> | Décalage de l’entrée de données <br/>   | Bit de poids fort 0. Adresse d’une entrée de données de ressource (feuille). <br/>                                                   |
| 4 <br/> | 4 <br/> | Décalage de sous-répertoire <br/> | Bit 1 élevé. Les 31 bits inférieurs sont l’adresse d’une autre table de répertoire de ressources (le niveau inférieur suivant). <br/> |



 

#### <a name="resource-directory-string"></a>Chaîne du répertoire de ressources

La zone de la chaîne du répertoire de ressources se compose de chaînes Unicode, alignées sur les mots. Ces chaînes sont stockées ensemble après la dernière entrée de répertoire de ressources et avant la première entrée de données de ressource. Cela réduit l’impact de ces chaînes de longueur variable sur l’alignement des entrées de répertoire de taille fixe. Chaque chaîne de répertoire de ressources a le format suivant :



| Offset        | Taille                 | Champ                      | Description                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Longueur <br/>         | Taille de la chaîne, sans inclure le champ de longueur lui-même. <br/> |
| 2 <br/> | variable <br/> | Chaîne Unicode <br/> | Données de chaîne Unicode de longueur variable, alignées sur les mots. <br/>     |



 

#### <a name="resource-data-entry"></a>Entrée de données de ressource

Chaque entrée de données de ressource décrit une unité réelle de données brutes dans la zone de données de ressource. Une entrée de données de ressource a le format suivant :



| Offset         | Taille          | Champ                            | Description                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA de données <br/>             | Adresse d’une unité de données de ressource dans la zone de données de ressource. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Taille <br/>                 | Taille, en octets, des données de ressource vers lesquelles pointe le champ de RVA de données. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Page de codes utilisée pour décoder les valeurs de point de code dans les données de ressource. En règle générale, la page de codes est la page de codes Unicode. <br/> |
| 12 <br/> | 4 <br/> | Réservé, doit avoir la valeur 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>Section. cormeta (objet uniquement)

Les métadonnées CLR sont stockées dans cette section. Il est utilisé pour indiquer que le fichier objet contient du code managé. Le format des métadonnées n’est pas documenté, mais peut être transmis aux interfaces CLR pour la gestion des métadonnées.

### <a name="the-sxdata-section"></a>Section. sxdata

Les gestionnaires d’exceptions valides d’un objet sont répertoriés dans la section **. sxdata** de cet objet. La section est marquée comme IMAGE \_ SCN \_ LNK \_ info. Il contient l’index de symboles COFF de chaque gestionnaire valide, en utilisant 4 octets par index.

En outre, le compilateur marque un objet COFF comme étant inscrit SEH en émettant le symbole absolu « @feat.00 » avec le LSB du champ de valeur défini sur 1. Un objet COFF sans gestionnaires SEH inscrits aurait le @feat.00 symbole «», mais pas la section **. sxdata** .

## <a name="archive-library-file-format"></a>Format de fichier d’archive (bibliothèque)

- [Signature du fichier d’archive](#archive-file-signature)
- [Archiver les en-têtes de membres](#archive-member-headers)
- [Premier membre de l’éditeur de liens](#first-linker-member)
- [Deuxième membre de l’éditeur de liens](#second-linker-member)
- [Membre Longnames](#longnames-member)

Le format d’archive COFF fournit un mécanisme standard pour le stockage des collections de fichiers objets. Ces collections sont communément appelées bibliothèques dans la documentation de programmation.

Les 8 premiers octets d’une archive sont composés de la signature de fichier. Le reste de l’archive est constitué d’une série de membres d’archive, comme suit :

-   Les premier et deuxième membres sont « membres de l’éditeur de liens ». Chacun de ces membres a son propre format comme décrit dans la section [type de nom d’importation](#import-name-type). En règle générale, un éditeur de liens place des informations dans ces membres d’archive. Les membres de l’éditeur de liens contiennent le répertoire de l’archive.

-   Le troisième membre est le membre « longnames ». Ce membre facultatif se compose d’une série de chaînes ASCII se terminant par un caractère null, dans lesquelles chaque chaîne est le nom d’un autre membre d’archive.

-   Le reste de l’archive est constitué de membres standard (fichier objet). Chacun de ces membres contient le contenu d’un fichier objet dans son intégralité.

Un en-tête de membre d’archive précède chaque membre. La liste suivante présente la structure générale d’une archive :

-   Signature : « ! &lt; arch &gt; \\ n»
-   En-tête

    <dl> premier membre de l’éditeur de liens  
    </dl>

-   En-tête

    <dl> 2e membre de l’éditeur de liens  
    </dl>

-   En-tête

    <dl> Membre Longnames  
    </dl>

-   En-tête

    <dl> Contenu du fichier OBJ 1  
    (Format COFF)  
    </dl>

-   En-tête

    <dl> Contenu du fichier OBJ 2  
    (Format COFF)  
    </dl>

### <a name="archive-file-signature"></a>Signature du fichier d’archive

La signature du fichier d’archive identifie le type de fichier. Tout utilitaire (par exemple, un éditeur de liens) qui prend un fichier d’archive comme entrée peut vérifier le type de fichier en lisant cette signature. La signature se compose des caractères ASCII suivants, dans lesquels chaque caractère ci-dessous est représenté littéralement, à l’exception du caractère de saut de ligne ( \\ n) :

`!<arch>\n`

### <a name="archive-member-headers"></a>Archiver les en-têtes de membres

Chaque membre (éditeur de liens, longnames ou membre de fichier objet) est précédé d’un en-tête. Un en-tête de membre d’archive a le format suivant, où chaque champ est une chaîne de texte ASCII qui est justifiée à gauche et complétée par des espaces à la fin du champ. Il n’y a pas de caractère null de fin dans l’un de ces champs.

Chaque en-tête de membre commence sur la première adresse paire après la fin du membre Archive précédent.



| Offset         | Taille           | Champ                     | Description                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Name <br/>          | Nom du membre d’archive, avec une barre oblique (/) ajoutée pour terminer le nom. Si le premier caractère est une barre oblique, le nom a une interprétation spéciale, comme décrit dans le tableau suivant. <br/> |
| 16 <br/> | 12 <br/> | Date <br/>          | Date et heure de création du membre d’archive : il s’agit de la représentation décimale ASCII du nombre de secondes écoulées depuis le 1/1/1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | ID d'utilisateur <br/>       | Représentation décimale ASCII de l’ID d’utilisateur. ce champ ne contient pas de valeur significative sur Windows plateformes, car les outils Microsoft émettent tous les espaces. <br/>                                    |
| 34 <br/> | 6 <br/>  | ID de groupe <br/>      | Représentation décimale ASCII de l’ID de groupe. ce champ ne contient pas de valeur significative sur Windows plateformes, car les outils Microsoft émettent tous les espaces. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Représentation octale ASCII du mode de fichier du membre. Il s’agit \_ de la valeur du mode St de la fonction Runtime C \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Taille <br/>          | Représentation décimale ASCII de la taille totale du membre d’archive, à l’exclusion de la taille de l’en-tête. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Fin d’en-tête <br/> | Les deux octets de la chaîne C « ̃ \\ n » (0X60 0x0A). <br/>                                                                                                                                               |



 

Le champ nom a l’un des formats répertoriés dans le tableau suivant. Comme mentionné précédemment, chacune de ces chaînes est alignée à gauche et complétée par des espaces de fin dans un champ de 16 octets :



| Contenu du champ de nom | Description                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nomme <br/>      | Nom du membre d’archive. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | Le membre archive est l’un des deux membres de l’éditeur de liens. Les deux membres de l’éditeur de liens portent ce nom. <br/>                                                                                                                                                                                          |
| // <br/>         | Le membre archive est le membre longnames, qui se compose d’une série de chaînes ASCII se terminant par null. Le membre longnames est le troisième membre Archive et est facultatif. <br/>                                                                     |
| /n <br/>         | Le nom du membre d’archive se trouve au décalage n dans le membre longnames. Le nombre n est la représentation décimale du décalage. Par exemple : « /26 » indique que le nom du membre d’archive se trouve à 26 octets au-delà du début du contenu du membre longnames. <br/> |



 

### <a name="first-linker-member"></a>Premier membre de l’éditeur de liens

Le nom du premier membre de l’éditeur de liens est « / ». Le premier membre de l’éditeur de liens est inclus à des fins de compatibilité descendante. Elle n’est pas utilisée par les éditeur de liens actuels, mais son format doit être correct. Ce membre de l’éditeur de liens fournit un répertoire de noms de symboles, comme le deuxième membre de l’éditeur de liens. Pour chaque symbole, les informations indiquent où trouver le membre d’archive contenant le symbole.

Le premier membre de l’éditeur de liens a le format suivant. Ces informations apparaissent après l’en-tête :



| Offset         | Taille               | Champ                         | Description                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Nombre de symboles <br/> | Unsigned long qui contient le nombre de symboles indexés. Ce nombre est stocké au format Big-endian. Chaque membre de fichier d’objet définit généralement un ou plusieurs symboles externes. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Décalages <br/>           | Tableau d’offsets de fichier pour archiver les en-têtes de membre, où n est égal au nombre de symboles. Chaque nombre dans le tableau est un entier long non signé, stocké au format Big-endian. Pour chaque symbole nommé dans la table de chaînes, l’élément correspondant dans le tableau offsets donne l’emplacement du membre d’archive qui contient le symbole. <br/> |
| \* <br/> | \* <br/>     | Table de chaînes <br/>      | Une série de chaînes terminées par le caractère null qui dénomment tous les symboles dans le répertoire. Chaque chaîne commence immédiatement après le caractère NULL dans la chaîne précédente. Le nombre de chaînes doit être égal à la valeur du champ nombre de symboles. <br/>                                                                                                       |



 

Les éléments du tableau offsets doivent être disposés par ordre croissant. Cela implique que les symboles de la table de chaînes doivent être organisés en fonction de l’ordre des membres d’archive. Par exemple, tous les symboles du premier membre de fichier objet doivent être listés avant les symboles dans le deuxième fichier objet.

### <a name="second-linker-member"></a>Deuxième membre de l’éditeur de liens

Le deuxième membre de l’éditeur de liens a le nom « / » comme le premier membre de l’éditeur de liens. Bien que les deux membres de l’éditeur de liens fournissent un répertoire des symboles et des membres d’archive qui les contiennent, le deuxième membre de l’éditeur de liens est utilisé de préférence au premier par tous les liens de l’éditeur de liens actuels. Le deuxième membre de l’éditeur de liens comprend des noms de symboles dans l’ordre lexical, ce qui permet une recherche plus rapide par nom.

Le deuxième membre a le format suivant. Ces informations apparaissent après l’en-tête :



| Offset         | Taille               | Champ                         | Description                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Nombre de membres <br/> | Valeur non signée de type long qui contient le nombre de membres d’archive. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Décalages <br/>           | Tableau d’offsets de fichier pour archiver les en-têtes de membre, organisés dans l’ordre croissant. Chaque décalage est un entier long non signé. Le nombre m est égal à la valeur du champ nombre de membres. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Nombre de symboles <br/> | Valeur non signée de type long qui contient le nombre de symboles indexés. Chaque membre de fichier d’objet définit généralement un ou plusieurs symboles externes. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Index <br/>           | Tableau d’index de base 1 (unsigned short) qui mappe les noms de symboles aux décalages de membres d’archive. Le nombre n est égal au nombre de champs de symboles. Pour chaque symbole qui est nommé dans la table de chaînes, l’élément correspondant dans le tableau d’index fournit un index dans le tableau offsets. Le tableau offsets indique à son tour l’emplacement du membre d’archive qui contient le symbole. <br/> |
| \* <br/> | \* <br/>     | Table de chaînes <br/>      | Une série de chaînes terminées par le caractère null qui dénomment tous les symboles dans le répertoire. Chaque chaîne commence immédiatement après l’octet NULL dans la chaîne précédente. Le nombre de chaînes doit être égal à la valeur du champ nombre de symboles. Ce tableau répertorie tous les noms de symboles dans l’ordre lexical croissant. <br/>                                                                             |



 

### <a name="longnames-member"></a>Membre Longnames

Le nom du membre longnames est « // ». Le membre longnames est une série de chaînes de noms de membres d’archive. Un nom apparaît ici uniquement lorsqu’il n’y a pas assez de place dans le champ nom (16 octets). Le membre longnames est facultatif. Il peut être vide avec uniquement un en-tête, ou il peut être complètement absent sans même en-tête.

Les chaînes se terminent par un caractère null. Chaque chaîne commence immédiatement après l’octet NULL dans la chaîne précédente.

## <a name="import-library-format"></a>Format de bibliothèque d’importation

- [Importer l’en-tête](#import-header)
- [Type d’importation](#import-type)

Les bibliothèques d’importation traditionnelles, autrement dit, les bibliothèques qui décrivent les exportations d’une image pour une utilisation par une autre, suivent généralement la disposition décrite dans la section 7, [format de fichier archive (bibliothèque)](#archive-library-file-format). La principale différence réside dans le fait que les membres de la bibliothèque d’importation contiennent des fichiers Pseudo-objets plutôt que des fichiers réels, dans lesquels chaque membre comprend les contributions de section requises pour créer les tables d’importation décrites dans la section 6,4, la section [. idata](#the-idata-section) l’éditeur de liens génère cette archive lors de la création de l’application d’exportation.

La section contributions pour une importation peut être déduite à partir d’un petit ensemble d’informations. L’éditeur de liens peut soit générer les informations complètes et détaillées dans la bibliothèque d’importation pour chaque membre au moment de la création de la bibliothèque, soit écrire uniquement les informations canoniques dans la bibliothèque et laisser l’application qui l’utilise ultérieurement générer les données nécessaires à la volée.

Dans une bibliothèque d’importation avec le format long, un seul membre contient les informations suivantes :

<dl> Archiver l’en-tête de membre  
En-tête de fichier  
En-têtes de section  
Données qui correspondent à chacun des en-têtes de section  
Table de symboles COFF  
Chaînes  
  
</dl>

En revanche, une petite bibliothèque d’importation est écrite comme suit :

<dl> Archiver l’en-tête de membre  
Importer l’en-tête  
Chaîne de nom d’importation terminée par un caractère null  
Chaîne de nom de DLL se terminant par un caractère null  
</dl>

Il s’agit d’informations suffisantes pour reconstruire avec précision la totalité du contenu du membre au moment de son utilisation.

### <a name="import-header"></a>Importer l’en-tête

L’en-tête d’importation contient les champs et décalages suivants :



| Offset         | Taille                | Champ                       | Description                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Le fichier IMAGE doit être un \_ \_ ordinateur \_ inconnu. Pour plus d’informations, consultez [types de machines](#machine-types). <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Doit être 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Version <br/>         | Version de la structure. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Machine <br/>         | Numéro qui identifie le type d’ordinateur cible. Pour plus d’informations, consultez [types de machines](#machine-types).<br/> |
| 8 <br/>  | 4 <br/>       | Marqueur de Time-Date <br/> | Date et heure de création du fichier. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Taille des données <br/>    | Taille des chaînes qui suivent l’en-tête. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinal/indicateur <br/>    | L’ordinal ou l’indicateur pour l’importation, déterminé par la valeur dans le champ type de nom. <br/>                   |
| 18 <br/> | 2 bits <br/>  | Type <br/>            | Type d’importation. Pour obtenir des descriptions et des valeurs spécifiques, consultez [type d’importation](#import-type).<br/>                           |
|                | 3 bits <br/>  | Type de nom <br/>       | Type de nom d’importation. Pour plus d’informations, consultez [importer le type de nom](#import-name-type). <br/>                           |
|                | 11 bits <br/> | Réservé <br/>        | Réservé, doit avoir la valeur 0. <br/>                                                                                             |



 

Cette structure est suivie de deux chaînes se terminant par un caractère null qui décrivent le nom du symbole importé et la DLL dont il provient.

### <a name="import-type"></a>Type d’importation

Les valeurs suivantes sont définies pour le champ type dans l’en-tête Import :

| Constante                  | Valeur         | Description                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTER le \_ code <br/>  | 0 <br/> | Code exécutable. <br/>                     |
| IMPORTER des \_ données <br/>  | 1 <br/> | Données. <br/>                                |
| IMPORTER \_ const <br/> | 2 <br/> | Spécifié comme CONSt dans le fichier. def. <br/> |

Ces valeurs sont utilisées pour déterminer les contributions de section qui doivent être générées par l’outil qui utilise la bibliothèque s’il doit accéder à ces données.

### <a name="import-name-type"></a>Type de nom d’importation

Le nom du symbole d’importation terminé par le caractère null suit immédiatement son en-tête d’importation associé. Les valeurs suivantes sont définies pour le champ type de nom dans l’en-tête d’importation. Ils indiquent comment le nom doit être utilisé pour générer les symboles corrects qui représentent l’importation :

| Constante | Valeur | Description |
| - | - | - |
| ORDINAL d’importation \_ | 0 | L’importation est par ordinal. Cela indique que la valeur du champ ordinal/indicateur de l’en-tête d’importation est l’ordinal de l’importation. Si cette constante n’est pas spécifiée, le champ ordinal/indication doit toujours être interprété comme l’indicateur de l’importation. |
| nom de l’importation \_ | 1 | Le nom d’importation est identique au nom du symbole public. |
| IMPORTER \_ le \_ préfixe de nom | 2 | Le nom d’importation est le nom de symbole public, mais il ignore le début, @ ou éventuellement \_ . |
| dédécorer le nom d’importation \_ \_ | 3 | Le nom d’importation est le nom du symbole public, mais ignore le début, @ ou éventuellement \_ , et tronque à la première @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Annexe A : calcul du hachage d’image PE Authenticode

- [Qu’est-ce qu’un hachage d’image PE Authenticode ?](#what-is-an-authenticode-pe-image-hash)
- [Qu’est-ce qui est couvert dans un hachage d’image PE Authenticode ?](#what-is-covered-in-an-authenticode-pe-image-hash)

Plusieurs certificats d’attribut sont censés être utilisés pour vérifier l’intégrité des images. Toutefois, la signature Authenticode la plus courante est. Une signature Authenticode peut être utilisée pour vérifier que les sections pertinentes d’un fichier image PE n’ont pas été modifiées à partir du formulaire d’origine du fichier. Pour accomplir cette tâche, les signatures Authenticode contiennent un nom de hachage d’image PE.

### <a name="what-is-an-authenticode-pe-image-hash"></a>Qu’est-ce qu’un hachage d’image PE Authenticode ?

Le hachage de l’image PE Authenticode, ou hachage de fichier pour Short, est similaire à une somme de contrôle de fichier en ce qu’il produit une petite valeur qui se réfère à l’intégrité d’un fichier. Une somme de contrôle est produite par un algorithme simple et est principalement utilisée pour détecter les défaillances de mémoire. Autrement dit, il est utilisé pour détecter si un bloc de mémoire sur le disque a disparu et que les valeurs stockées sont endommagées. Un hachage de fichier est similaire à une somme de contrôle en ce qu’il détecte également une altération de fichier. Toutefois, contrairement à la plupart des algorithmes de somme de contrôle, il est très difficile de modifier un fichier afin qu’il ait le même hachage de fichier que sa forme d’origine (non modifiée). Autrement dit, une somme de contrôle est conçue pour détecter les défaillances de mémoire simples qui entraînent une altération, mais un hachage de fichier peut être utilisé pour détecter des modifications intentionnelles et même subtiles d’un fichier, telles que celles introduites par des virus, des pirates ou des programmes de cheval de Troie.

Dans une signature Authenticode, le hachage de fichier est signé numériquement à l’aide d’une clé privée connue uniquement du signataire du fichier. Un consommateur de logiciels peut vérifier l’intégrité du fichier en calculant la valeur de hachage du fichier et en le comparant à la valeur du hachage signé contenu dans la signature numérique Authenticode. Si les hachages de fichier ne correspondent pas, une partie du fichier couvert par le hachage d’image PE a été modifiée.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>Qu’est-ce qui est couvert dans un hachage d’image PE Authenticode ?

Il n’est pas possible ou souhaitable d’inclure toutes les données du fichier image dans le calcul du hachage de l’image PE. Parfois, il présente simplement des caractéristiques indésirables (par exemple, les informations de débogage ne peuvent pas être supprimées des fichiers publiés publiquement). parfois, il est tout simplement impossible. Par exemple, il n’est pas possible d’inclure toutes les informations dans un fichier image dans une signature Authenticode, puis d’insérer la signature Authenticode qui contient ce hachage d’image PE dans l’image PE, puis de générer un hachage d’image PE identique en incluant à nouveau toutes les données de fichier image dans le calcul, car le fichier contient maintenant la signature Authenticode qui n’était pas à l’origine.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Processus de génération du hachage d’image PE Authenticode

Cette section décrit comment un hachage d’image PE est calculé et quelles parties de l’image PE peuvent être modifiées sans invalider la signature Authenticode.

> [!NOTE]
> Le hachage de l’image PE d’un fichier spécifique peut être inclus dans un fichier catalogue distinct sans inclure un certificat d’attribut dans le fichier haché. Cela est pertinent, car il devient possible d’invalider le hachage de l’image PE dans un fichier de catalogue signé par Authenticode en modifiant une image PE qui ne contient pas réellement de signature Authenticode.

Toutes les données des sections de l’image PE qui sont spécifiées dans la table de section sont hachées dans leur intégralité, à l’exception des plages d’exclusion suivantes :

- **champ de la somme de contrôle de fichier des champs spécifiques au Windows de l’en-tête facultatif.** Cette somme de contrôle inclut le fichier entier (y compris tous les certificats d’attribut dans le fichier). Dans toutes les éventualités, la somme de contrôle sera différente de la valeur d’origine après l’insertion de la signature Authenticode.

- **Informations relatives aux certificats d’attribut**. Les zones de l’image PE qui sont associées à la signature Authenticode ne sont pas incluses dans le calcul du hachage d’image PE, car les signatures Authenticode peuvent être ajoutées ou supprimées d’une image sans affecter l’intégrité globale de l’image. Ce n’est pas un problème, car il existe des scénarios utilisateur qui dépendent de la nouvelle signature d’images PE ou de l’ajout d’un horodatage. Authenticode exclut les informations suivantes du calcul de hachage :

  - Champ de la table de certificats des répertoires de données d’en-tête facultatifs.

  - La table de certificats et les certificats correspondants pointés par le champ de table de certificat répertorié juste au-dessus.

  Pour calculer le hachage de l’image PE, Authenticode ordonne les sections spécifiées dans la table de section par plage d’adresses, puis hache la séquence d’octets obtenue, en passant par les plages d’exclusion.

- **Informations au-delà de la fin de la dernière section.** La zone située au-delà de la dernière section (définie par le décalage le plus élevé) n’est pas hachée. Cette zone contient généralement des informations de débogage. Les informations de débogage peuvent généralement être considérées comme des conseils aux débogueurs. elle n’affecte pas l’intégrité réelle du programme exécutable. Il est tout à fait possible de supprimer les informations de débogage d’une image après la remise d’un produit et de ne pas affecter la fonctionnalité du programme. En fait, cette opération est parfois effectuée sous la forme d’une mesure d’enregistrement sur disque. Il est à noter que les informations de débogage contenues dans les sections spécifiées de l’image PE ne peuvent pas être supprimées sans invalider la signature Authenticode.

vous pouvez utiliser les outils makecert et signtool fournis dans le kit de développement logiciel (SDK) de la plateforme Windows pour expérimenter la création et la vérification des signatures Authenticode. Pour plus d’informations, consultez Référence, ci-dessous.

## <a name="references"></a>Références

[téléchargements et outils pour Windows (y compris le SDK Windows)](https://developer.microsoft.com/windows/downloads)

[Création, affichage et gestion des certificats](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Procédure pas à pas de signature de code en mode noyau (.doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Windows Format de signature exécutable portable Authenticode (.docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Fonctions ImageHlp](/windows/desktop/Debug/imagehlp-functions)
