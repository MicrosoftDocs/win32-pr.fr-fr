---
description: Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un fichier d’archive de texte, le fichier. IDT respecte le format de fichier d’archive de base.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Données ASCII dans les fichiers d’archive de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7fa327d19b59793862bd2c06ce814b17979e8e8a6f72d41b1af677b715b4ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078069"
---
# <a name="ascii-data-in-text-archive-files"></a>Données ASCII dans les fichiers d’archive de texte

Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un [fichier d’archive de texte](text-archive-files.md), le fichier. IDT respecte le format de fichier d' [Archive](archive-file-format.md)de base. Si la table contient des informations non-ASCII, le format du fichier d’archive est étendu pour inclure les informations de la page de codes.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Fichiers d’archive de texte qui contiennent uniquement des caractères ASCII

Lorsqu’une table qui contient uniquement des caractères ASCII est exportée vers un fichier d’archive, le fichier. IDT est au [format de fichier d’archive](archive-file-format.md)de base. Chaque flux de la table est exporté sous la forme d’un fichier avec une extension de nom de fichier. IBD. Les fichiers. IBD sont stockés dans un dossier portant le même nom que la table. Par exemple, considérez l’exportation de la table [binaire](binary-table.md) suivante.



| Name  | Données      |
|-------|-----------|
| Livres | Books. IBD |
| Voitures  | Cars. IBD  |



 

La structure de répertoire après l’exportation de cette table est la suivante. Les informations de la table de base de données sont exportées vers Binary. IDT. Les deux flux de données binaires sont exportés vers Book. IBD et cars. IBD enregistrés dans le dossier nommé Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Le fichier d’archive binaire. IDT est au [format de fichier d’archive](archive-file-format.md) de base et se présente comme suit.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Fichiers d’archive de texte contenant des caractères non-ASCII

Si le fichier contient des données non-ASCII, le [format de fichier d’archive](archive-file-format.md) de base du fichier. IDT est étendu pour inclure les informations de la page de codes. La troisième ligne de la table. IDT est la page de codes numérique suivie du nom de la table et des noms de colonne de clé primaire séparés par des tabulations.

> [!Note]  
> Un fichier. IDT qui contient des informations non-ASCII doit être enregistré au format ASCII. Par exemple, un fichier d’archive de texte peut contenir les noms de colonne et de table encodés au format UTF-8, mais le fichier d’archive lui-même doit être au format ASCII.

 

La table ActionText suivante localisée en français contient des informations non-ASCII. La page de codes numérique utilisée pour les chaînes françaises est 1252.



| Action    | Description                                  | Modèle |
|-----------|----------------------------------------------|----------|
| PUBLIER | Publication d’infos sur l’application |          |



 

Le fichier d’archive exporté, ActionText. IDT, est le suivant.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Si un fichier d’archive de texte contient des données non-ASCII, le fichier d’archive inclut des informations sur la page de codes. Les fichiers d’archive avec les informations de page de codes peuvent être réimportés uniquement dans une base de données de la page de codes exacte ou dans une base de données indépendante de la langue. Dans le cas d’une base de données indépendante de la langue, la page de codes est définie sur la page de codes du fichier d’archive. pour plus d’informations sur la façon dont Windows Installer gère les pages de codes, consultez la section [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



