---
title: Grammaire
description: Les instructions HLSL sont construites à l’aide des règles suivantes pour la grammaire.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507735"
---
# <a name="grammar"></a>Grammaire

Les instructions HLSL sont construites à l’aide des règles suivantes pour la grammaire.

-   [Espace blanc](#whitespace)
-   [Nombres à virgule flottante](#floating-point-numbers)
-   [Nombres entiers](#integer-numbers)
-   [Caractères](#characters)
-   [Chaînes](#strings)
-   [Identificateurs](#identifiers)
-   [Opérateurs](#operators)
-   [Rubriques connexes](#related-topics)

## <a name="whitespace"></a>Espace blanc

Les caractères suivants sont reconnus comme des espaces blancs.



|                            |
|----------------------------|
| SPACE                      |
| Tab                        |
| ÉCHÉANCE                        |
| Commentaires de style C (/ \* \* /) |
| Commentaires de style C++ (//)    |



 

## <a name="floating-point-numbers"></a>Nombres à virgule flottante

Les nombres à virgule flottante sont représentés en langage HLSL comme suit :

-   fraction-constante de l’exposant-partie (opt)-suffixe à virgule flottante (opt)

    digit-Sequence-suffixe à virgule flottante de partie exposant (opt)

-   fraction-constante :

    chiffre-séquence (opt). digit-sequence

    chiffre-séquence.

-   partie exposant :

    chiffre e (opt)-séquence

    Chiffre E (opt)-séquence

-   sign : un des éléments suivants

    \+ -

-   chiffre-séquence :

    digit

    digit-sequence digit

-   floating-suffix : un des éléments suivants

    h H f F l

    Utilisez le suffixe « L » pour spécifier un littéral à virgule flottante de précision 64 bits complet. Un littéral de virgule flottante de 32 bits est la valeur par défaut.

    Par exemple, le compilateur reconnaît la valeur littérale suivante comme un littéral à virgule flottante de précision 32 bits et ignore les bits inférieurs :

    ```
    double x = -0.6473313946860445;
    ```

    

    Le compilateur reconnaît la valeur littérale suivante comme un littéral à virgule flottante de précision 64 bits :

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Nombres entiers

Les nombres entiers sont représentés en langage HLSL comme suit :

-   entier-constante entier-suffixe (opt)
-   Integer-constante : un des éléments suivants :

    \# (nombre décimal)

    0 \# (nombre octal)

    0x \# (nombre hexadécimal)

-   le suffixe entier peut être l’un des éléments suivants :

    u U l L

## <a name="characters"></a>Caractères

Les caractères sont représentés en langage HLSL comme suit :



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| « c »                                       | symbole                                                     |
| ' \\ a' ' \\ b' ' \\ f' ' \\ b' ' \\ r' ' \\ t' ' \\ v' | d’échappement                                                       |
| '\\\#\#\#'                                | (échappement octal, chacun \# est un chiffre octal)                       |
| ' \\ x \# '                                   | (caractère d’échappement hexadécimal, \# est un nombre hexadécimal, un nombre quelconque de chiffres)            |
| ' \\ c'                                     | (c est un autre caractère, y compris une barre oblique inverse et des guillemets) |



 

Les séquences d’échappement ne sont pas prises en charge dans les expressions de préprocesseur.

## <a name="strings"></a>Chaînes

Les chaînes sont représentées en langage HLSL comme suit :

« s » (s est une chaîne avec échappements).

## <a name="identifiers"></a>Identificateurs

Les identificateurs sont représentés en langage HLSL comme suit :


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Opérateurs


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



Également tout autre caractère unique qui ne correspondait pas à une autre règle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annexe (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




