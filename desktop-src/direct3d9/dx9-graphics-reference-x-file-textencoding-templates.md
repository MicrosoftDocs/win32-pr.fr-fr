---
description: 'Les modèles définissent la façon dont le flux de données est interprété : les données sont modulées par la définition du modèle. Cette section décrit les aspects suivants d’un modèle et fournit un exemple de modèle.'
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modèles (format de fichier X, encodage de texte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745389"
---
# <a name="templates-x-file-format-text-encoding"></a>Modèles (format de fichier X, encodage de texte)

Les modèles définissent la façon dont le flux de données est interprété : les données sont modulées par la définition du modèle. Cette section décrit les aspects suivants d’un modèle et fournit un exemple de modèle.

Il existe un modèle spécial : le modèle d’en-tête. Il est recommandé que chaque application définisse un modèle d’en-tête et l’utilise pour définir des informations spécifiques à l’application, telles que des informations de version. S’il est présent, cet en-tête est lu par l’API de format de fichier. x. Si un membre indicateurs est disponible, il est utilisé pour déterminer comment les données suivantes sont interprétées. Le membre Flags, s’il est défini, doit être une valeur DWORD. Un bit est actuellement défini-bit 0. Si ce bit est clair, les données suivantes dans le fichier sont binaires. Si cette valeur est définie, les données suivantes sont du texte. Vous pouvez utiliser plusieurs objets de données d’en-tête pour basculer entre le binaire et le texte dans le fichier.

## <a name="template-form-name-and-uuid"></a>Formulaire, nom et UUID du modèle

Un modèle se présente sous la forme suivante.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



Le nom du modèle est un nom alphanumérique qui peut inclure le trait de soulignement ( \_ ). Il ne doit pas commencer par un chiffre. L’UUID est un identificateur unique universel mis en forme dans l’environnement de calcul distribué (Open Software Foundation) standard et placé entre crochets (< >). Par exemple : <> 3D82AB43-62DA-11cf-AB39-0020AF71E433.

## <a name="template-members"></a>Membres du modèle

Les membres de modèles se composent d’un type de données nommé suivi d’un nom facultatif ou d’un tableau d’un type de données nommé. Les types de données primitifs valides sont définis dans le tableau suivant.



| Type    | Taille                               |
|---------|------------------------------------|
| WORD    | 16 bits                            |
| DWORD   | 32 bits                            |
| FLOAT   | FLOTTE IEEE                         |
| DOUBLE  | 64 bits                            |
| CHAR    | 8 bits                             |
| UCHAR   | 8 bits                             |
| BYTE    | 8 bits                             |
| STRING  | Chaîne terminée par NULL             |
| CSTRING | Chaîne C mise en forme (non prise en charge) |
| UNICODE | Chaîne Unicode (non prise en charge)     |



 

Les types de données supplémentaires définis par les modèles rencontrés précédemment dans le flux de données peuvent également être référencés dans une définition de modèle. Aucune référence anticipée n’est autorisée.

Tous les types de données valides peuvent être exprimés sous la forme d’un tableau dans la définition du modèle. La syntaxe de base est illustrée dans l’exemple suivant.


```
array <data-type> <name>[<dimension-size>];
```



<dimension-size> peut être un entier ou une référence nommée à un autre membre de modèle dont la valeur est ensuite substituée. Les tableaux peuvent être multidimensionnels, où n est déterminé par le nombre de crochets appariés à la fin de l’instruction, comme dans l’exemple suivant.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Restrictions de modèle

Les modèles peuvent être ouverts, fermés ou restreints. Ces restrictions déterminent les types de données qui peuvent apparaître dans la hiérarchie immédiate d’un objet de données défini par le modèle. Un modèle ouvert n’a aucune restriction, un modèle fermé rejette tous les types de données et un modèle restreint autorise une liste nommée de types de données.

La syntaxe permettant d’indiquer qu’un modèle est ouvert est de trois points délimités par des crochets.


```
[ ... ]
```



Une liste séparée par des virgules de types de données nommés suivi éventuellement de leurs UUID délimités par des crochets indique un modèle restreint.


```
[ { data-type [ UUID ] , } ... ]
```



L’absence de l’un des éléments ci-dessus indique un modèle fermé.

## <a name="template-example"></a>Exemple de modèle

L’exemple suivant montre un exemple de modèle.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage de texte](text-encoding.md)
</dt> </dl>

 

 



