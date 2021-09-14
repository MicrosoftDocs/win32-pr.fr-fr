---
title: Transmit_as et Represent_as
description: Transmettre \_ en tant que et représenter \_ comme partage la même disposition, à l’exception du jeton de début ; le jeton lit FC \_ transmit \_ As ou FC \_ représente \_ comme, mais le code sous-jacent est courant.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011406"
---
# <a name="transmit_as-and-represent_as"></a>Transmettre \_ en tant que et représenter \_ comme

Transmettre \_ en tant que et représenter \_ comme partage la même disposition, à l’exception du jeton de début ; le jeton lit FC \_ transmit \_ As ou FC \_ représente \_ comme, mais le code sous-jacent est courant.

La description présente la disposition suivante :

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Les indicateurs<1> octet se composent du Quartet indicateur supérieur et du Quartet alignement inférieur.

Le grignot d’alignement conserve l’alignement filaire du type transmis. Cela est nécessaire lorsque le dimensionnement de la mémoire tampon et l’utilisation de la taille de type transmis à partir du code de format.

L’indicateur Quartet peut avoir les indicateurs suivants :

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

Le \_ type présenté \_ est \_ un indicateur de tableau qui marque une transmission de niveau supérieur en tant qu’argument (ou représente en tant que) comme un tableau d’éléments et une valeur passée. L’interpréteur [**– OI**](/windows/desktop/Midl/-oi) utilise cet indicateur pour effectuer un pas à pas principal de ce type d’argument (qui est en fait un pointeur sur Stack, et non sur le tableau). Les deux autres indicateurs sont également utilisés uniquement dans les interpréteurs précédents pour effectuer un pas à pas détaillé sur un type présenté sur la pile.

L' \_ index quintuple<2> est un index de la routine de rappel quintuple (il s’agit en fait d’un quadruple) de fonctions. La table est commune à la fois à transmit As et à replacer en tant que et il existe un mappage évident pour la position des routines, étant donné que le même service de points d’entrée transmet les codes et les représente comme des codes. Le mappage est de \_ local => à transmission \_ , à \_ local => de transmission \_ , Free \_ inst => transmission gratuite \_ , Free \_ local => Free \_ inst.

La \_ \_ \_ taille de mémoire de type présentée<2> fournit toujours une taille pour le type présenté/local, y compris les types de représentation inconnus.

La taille de la \_ mémoire tampon de type transmis \_ \_<2> est égale à zéro, lorsque la taille est variable ou la taille fixe réelle. Il s’agit d’une optimisation qui permet d’ignorer certains rappels lors du dimensionnement de la mémoire tampon.

Le \_ décalage de type transmis \_<2> est le décalage de type relatif habituel par rapport à la chaîne de format de type transmis.

 

 