---
title: C-problèmes de compression du compilateur
description: Les niveaux de compression affectent la disposition de la mémoire des types pour MIDL et le compilateur Microsoft C/C++ de la même façon.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL du compilateur MIDL, problèmes d’empaquetage du compilateur C
- compression MIDL
- configuration de la mémoire (MIDL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d355214c7f3222d67fd7673de4f9d32d19b4c885e8f97143c80df7b98bc0e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807892"
---
# <a name="c-compiler-packing-issues"></a>C-problèmes de compression du compilateur

Les niveaux de compression affectent la disposition de la mémoire des types pour MIDL et le compilateur Microsoft C/C++ de la même façon. dans les environnements de génération Microsoft, tels que l’environnement de génération défini par VC++ ou le kit de développement logiciel (SDK) de la plateforme, le niveau de compression par défaut pour les compilateurs MIDL et C/C++ est le même ; le niveau de compression par défaut pour les environnements de génération de Windows 32 bits et 64 bits est 8.

## <a name="natural-alignment"></a>Alignement naturel

Pour les types en mémoire, l’alignement par défaut est identique à son alignement naturel.

-   Un type de base, tel que Short, float et \_ \_ Int64, et un pointeur sont alignés naturellement si sa représentation commence à une adresse qui est modulo sa taille. Tous les types de base actuellement pris en charge ont des tailles de 1, 2, 4 ou 8. Les pointeurs ont une taille de 4 dans les environnements 32 bits et 8 dans les environnements 64 bits.
-   Un type composé est aligné naturellement si chacun de ses composants est aligné naturellement par rapport au début du type, et s’il n’y a pas d’écarts inutiles (remplissage) entre les composants. Les composants composés, tels que les champs ou les éléments, sont récursifs pour les composants de type pointeur ou de base.

Une règle simple pour vous aider à mémoriser ce comportement est que l’alignement naturel d’un type est égal aux alignements les plus importants de ses composants.

Il existe une connexion entre l’alignement et la taille de la mémoire d’un type dans des langages tels que C ou C++ et IDL, comme exprimé par l’opérateur **sizeof ()**. La taille est un multiple de l’alignement (le multiple minimal qui couvre le type). Cela suit à partir d’une représentation sous forme de tableau dans la mémoire.

L’alignement naturel est important car l’accès aux données mal alignées peut provoquer une exception sur certains systèmes. Les données peuvent être marquées pour une manipulation sécurisée lorsqu’elles sont mal alignées, mais cela implique généralement une pénalité de vitesse qui peut être importante sur certaines plateformes.

> [!Note]  
> En mémoire, les objets de types avec un alignement naturel de *n* sont garantis correctement alignés lorsqu’ils sont placés à des adresses qui sont un multiple de *n*.

 

## <a name="packing-versus-alignment"></a>Compression et alignement

La spécification d’un niveau de compactage supérieur à l’alignement naturel d’un type ne change pas l’alignement du type. La spécification d’un niveau de compactage plus petit que l’alignement naturel réduit l’alignement du type au niveau de la compression. Par conséquent, les types compressés peuvent être placés en mémoire sur des adresses qui sont un multiple du niveau de compression (alignement réduit) sans entraîner de mauvais alignement. Cela affecte à la fois les types simples et les types de composants. Pour les types composés, la disposition interne du type peut être affectée, car l’alignement réduit des composants peut modifier la taille de la marge intérieure nécessaire à l’alignement correct des composants, réduisant ainsi la taille du type.

Une règle simple pour vous aider à mémoriser ce comportement est que le nouvel alignement d’un type condensé est le plus petit du niveau de compression et son alignement naturel. La taille du type est un multiple du nouvel alignement. L’opérateur **sizeof ()** retourne la taille réduite pour les types compressés.

Par exemple, avec le niveau de compression 2, un long est aligné sur 2 et peut donc être placé à toute adresse paire, non seulement aux adresses qui sont un multiple de 4 comme c’est le cas avec l’alignement naturel. Une structure avec un short et un long, compressée à 2, n’a pas besoin de l’intervalle interne entre le short et le long suivant, nécessaire pour l’alignement naturel ; par conséquent, non seulement la structure est maintenant alignée sur 2, mais elle a également une taille réduite de 8 à 6.

Par exemple, considérez un type composé constitué d’un caractère codé sur 1 octet, d’un entier de 4 octets et d’un caractère de 1 octet :

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

Cette structure est naturellement alignée sur 4 et a une taille naturelle de 12.

Pour le niveau de compression 4 ou supérieur, la structure **MyStruct** est alignée sur 4 et `sizeof(struct mystructtype)` est égale à 12. La structure sera mal alignée si elle se trouve en mémoire à une adresse qui n’est pas un multiple de 4.

Pour le niveau de compression 2, la structure est alignée sur 2 et sa taille est 8. La structure compressée avec le niveau 2 sera mal alignée si elle se trouve en mémoire à une adresse qui n’est pas un multiple de 2.

Pour le niveau de compression 1, la structure est alignée sur 1 et sa taille est 6. La structure compressée avec le niveau 1 peut être placée n’importe où sans entraîner une erreur d’alignement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[/ZP](./-zp.md)
</dt> <dt>

[/Pack](./-pack.md)
</dt> </dl>

 

 