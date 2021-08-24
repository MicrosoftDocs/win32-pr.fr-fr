---
description: Toutes les polices utilisent un jeu de caractères. Un jeu de caractères contient des signes de ponctuation, des chiffres, des lettres majuscules et minuscules, ainsi que tous les autres caractères imprimables. Chaque élément d’un jeu de caractères est identifié par un nombre.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Jeux de caractères utilisés par les polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ec30a82c08a0b9ac1162034b6308bb68ff7dc1c6469e5e73bad2838b528eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779359"
---
# <a name="character-sets-used-by-fonts"></a>Jeux de caractères utilisés par les polices

Toutes les polices utilisent un jeu de caractères. Un jeu de caractères contient des signes de ponctuation, des chiffres, des lettres majuscules et minuscules, ainsi que tous les autres caractères imprimables. Chaque élément d’un jeu de caractères est identifié par un nombre.

La plupart des jeux de caractères en cours d’utilisation sont des superséries du jeu de caractères ASCII (États-Unis), qui définissent les caractères des valeurs numériques 96 de 32 à 127. Il existe cinq groupes principaux de jeux de caractères :

-   Windows
-   Unicode
-   OEM (fabricant de l’équipement d’origine)
-   Symbole
-   Spécifique au fournisseur

## <a name="windows-character-set"></a>Windows Jeu de caractères

le jeu de caractères Windows est le jeu de caractères le plus couramment utilisé. Elle est essentiellement équivalente au jeu de caractères ANSI. le caractère vide est le premier caractère du jeu de caractères Windows. Sa valeur hexadécimale est 0x20 (décimal 32). le dernier caractère du jeu de caractères Windows a une valeur hexadécimale de 0xff (décimal 255).

De nombreuses polices spécifient un caractère par défaut. Chaque fois qu’une demande est effectuée pour un caractère qui n’est pas dans la police, le système fournit ce caractère par défaut. de nombreuses polices utilisant le jeu de caractères Windows spécifient le point (.) comme caractère par défaut. Les polices TrueType et OpenType utilisent généralement une zone ouverte comme caractère par défaut.

Les polices utilisent un caractère de saut de ligne appelé quadruple pour séparer les mots et justifier le texte. la plupart des polices utilisant le jeu de caractères Windows spécifient que le caractère vide sera utilisé comme caractère de saut de ligne.

## <a name="unicode-character-set"></a>Jeu de caractères Unicode

le jeu de caractères Windows utilise 8 bits pour représenter chaque caractère ; par conséquent, le nombre maximal de caractères qui peuvent être exprimés à l’aide de 8 bits est 256 (2 ^ 8). Cela est généralement suffisant pour les langues occidentales, y compris les signes diacritiques utilisés en français, en allemand, en espagnol et dans d’autres langues. Toutefois, les langues orientales utilisent des milliers de caractères distincts, qui ne peuvent pas être encodés à l’aide d’un schéma de codage codé sur un octet. Avec la prolifération des ordinateurs de commerce informatisé, les schémas de codage sur deux octets ont été développés afin que les caractères puissent être représentés en séquences 8 bits, 16 bits, 24 bits ou 32 bits. Cela nécessite des algorithmes de passage compliqués ; même dans ce cas, l’utilisation de différents jeux de code peut produire des résultats entièrement différents sur deux ordinateurs différents.

Pour résoudre le problème de plusieurs schémas de codage, la norme Unicode pour la représentation des données a été développée. Un schéma de codage de caractères de 16 bits, Unicode peut représenter 65 536 (2 ^ 16) caractères, ce qui suffit pour inclure toutes les langues du commerce informatique aujourd’hui, ainsi que des signes de ponctuation, des symboles mathématiques et de l’espace pour l’extension. Unicode établit un code unique pour chaque caractère afin de garantir que la traduction des caractères est toujours exacte.

## <a name="oem-character-set"></a>Jeu de caractères OEM

Le jeu de caractères OEM est généralement utilisé dans les sessions MS-DOS en plein écran pour l’affichage à l’écran. les caractères 32 à 127 sont généralement les mêmes dans les jeux de caractères OEM, ASCII (états-unis) et Windows. Les autres caractères dans le jeu de caractères OEM (0 à 31 et 128 à 255) correspondent aux caractères qui peuvent être affichés dans une session MS-DOS en plein écran. ces caractères sont généralement différents des caractères de Windows.

## <a name="symbol-character-set"></a>Jeu de caractères de symbole

Le jeu de caractères de symbole contient des caractères spéciaux généralement utilisés pour représenter des formules mathématiques et scientifiques.

## <a name="vendor-specific-character-sets"></a>Jeux de caractères spécifiques au fournisseur

de nombreuses imprimantes et autres périphériques de sortie fournissent des polices basées sur des jeux de caractères qui diffèrent du Windows et de l’exemple OEM setsfor, le jeu de caractères Extended Binary Coded Decimal Interchange Code (EBCDIC). pour utiliser l’un de ces jeux de caractères, le pilote d’imprimante convertit le jeu de caractères Windows en jeu de caractères spécifique au fournisseur.

 

 



