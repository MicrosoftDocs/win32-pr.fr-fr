---
description: un fichier d’archive de texte pour une base de données Windows Installer comporte une extension de nom de fichier. idt.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Format de fichier d’archive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092614"
---
# <a name="archive-file-format"></a>Format de fichier d’archive

un [fichier d’archive de texte](text-archive-files.md) pour une base de données Windows Installer comporte une extension de nom de fichier. idt. Lorsqu’une base de données entière est exportée vers des fichiers d’archive, chaque table de la base de données a un fichier. IDT distinct. Si une table contient une colonne de flux, chaque flux de la table est représenté par un fichier avec une extension de nom de fichier. IBD. Les fichiers. IBD sont stockés dans un dossier portant le même nom que la table.

## <a name="idt-file-format"></a>Format de fichier. IDT

Le fichier. IDT d’une table de base de données exportée qui contient uniquement des caractères ASCII a le format de base suivant.

-   La première ligne contient les noms de colonnes de table séparés par des tabulations.
-   La deuxième ligne contient les définitions de colonne séparées par des tabulations.
-   Si le fichier contient uniquement des données ASCII, la troisième ligne est le nom de la table et les noms de colonne de clé primaire séparés par des tabulations.
-   Les lignes restantes dans le fichier représentent des lignes de la table, avec des colonnes séparées par des tabulations.

> [!Note]  
> Si le fichier contient des données non-ASCII, la troisième ligne correspond à la page de codes numérique suivie du nom de la table et des noms de colonne de clé primaire séparés par des tabulations. Un fichier. IDT qui contient des informations non-ASCII doit être enregistré au format ASCII. Par exemple, un fichier d’archive de texte peut contenir les noms de colonne et de table encodés au format UTF-8, mais le fichier d’archive lui-même doit être au format ASCII. Consultez la section [données ASCII dans les fichiers d’archive de texte](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> Les fichiers [ \_ ForceCodepage](-forcecodepage.md) et [ \_ SummaryInformation](-summaryinformation.md) . IDT spéciaux utilisent des formats étendus. Consultez les \_ sections ForceCodepage et \_ SummaryInformation pour obtenir une description de leurs formats.

 

## <a name="column-definitions"></a>Définitions de colonne

Les définitions de colonne sont indiquées par des caractères.

-   Le premier caractère indique le type de colonne. Une lettre minuscule indique une colonne qui n’accepte pas les valeurs NULL et une lettre majuscule indique que la colonne peut contenir des valeurs NULL.

    | Caractère | Signification                   |
    |-----------|---------------------------|
    | s, S      | Colonne de chaîne             |
    | l, L      | Colonne de chaîne localisable |
    | v, V      | Colonne binaire             |
    | Je vais      | Colonne d’entiers            |

    

     

-   Le deuxième caractère indique la taille des données de la colonne.

    > [!Note]  
    > la Windows Installer n’utilise pas réellement la taille de colonne spécifiée pour limiter la taille de la chaîne qui peut être entrée dans un champ de colonne de chaîne. Toutefois, certains outils de création utilisent la taille de colonne spécifiée pour limiter la taille d’une chaîne valide. Il est recommandé que les chaînes entrées dans une colonne répondent à l’exigence de taille spécifiée.

     

    

    | Définition de colonne | Signification                                    |
    |-------------------|--------------------------------------------|
    | s255              | Colonne de chaîne non Nullable 255 longue        |
    | L50               | Colonne de chaîne localisable Nullable 50 long |
    | I2, I2            | Colonne de type entier Short                       |
    | I4, I4            | Colonne de type entier long                        |

    

     

## <a name="control-character-translation"></a>Conversion de caractères de contrôle

L’exportation d’une table dans un fichier d’archive de texte traduit les caractères de contrôle pour éviter les conflits avec les délimiteurs de fichiers. Lors de l’écriture dans le fichier. IDT, les caractères de contrôle sont convertis comme suit.



| Caractère de contrôle | Traduction dans. IDT | Signification         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Espace arrière      |
| HT                | 16                  | Onglet             |
| CHARIOT                | 25                  | Saut de ligne       |
| FF                | 24                  | Saut de page       |
| CR                | 17                  | Retour chariot |



 

 

 



