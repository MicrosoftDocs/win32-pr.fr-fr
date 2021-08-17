---
title: " Directives if, Elif, Else et endif"
description: Directives de préprocesseur qui contrôlent la compilation des parties d’un fichier source.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Directives HLSL, if, Elif, Else et endif
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726449"
---
# <a name="if-elif-else-and-endif-directives"></a>\#Directives if, \# Elif, \# else et \# endif

Directives de préprocesseur qui contrôlent la compilation des parties d’un fichier source.



| \#Si *ifCondition* ...         |
|--------------------------------|
| \[\#*elifCondition* elif...\] |
| \[\#sinon...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condition principale à évaluer. Si ce paramètre a une valeur différente de zéro, tout le texte entre cette \# directive if et l’instance suivante de la \# directive Elif, \# else ou \# endif est conservé dans l’unité de traduction ; sinon, le code source suivant n’est pas conservé. <br/> La condition peut utiliser l’opérateur de préprocesseur défini pour déterminer si une constante ou une macro de préprocesseur spécifique est définie ; cette utilisation est équivalente à l’utilisation de la directive [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Consultez la section Notes pour connaître les restrictions relatives à la valeur du paramètre *ifCondition* . <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ facultatif\] <br/> | Autre condition à évaluer. Si le paramètre *ifCondition* et toutes les \# directives Elif précédentes ont la valeur zéro et que ce paramètre a une valeur différente de zéro, tout le texte entre cette \# directive elif et l’instance suivante de la \# directive Elif, \# else ou \# endif est conservé dans l’unité de traduction ; sinon, le code source suivant n’est pas conservé. <br/> La condition peut utiliser l’opérateur de préprocesseur défini pour déterminer si une constante ou une macro de préprocesseur spécifique est définie ; cette utilisation est équivalente à l’utilisation de la directive [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Consultez la section Notes pour connaître les restrictions relatives à la valeur du paramètre *elifCondition* . <br/> |



 

## <a name="remarks"></a>Remarques

Chaque \# directive if dans un fichier source doit être mise en correspondance par une \# directive de fermeture endif. Un nombre quelconque de \# directives Elif peuvent apparaître entre les \# directives if et \# endif, mais au plus une \# directive else est autorisée. La \# directive else, le cas échéant, doit être la dernière directive avant \# endif. Les directives de compilation conditionnelle contenues dans les fichiers include doivent respecter les mêmes conditions.

Les \# directives if, \# Elif, \# else et \# endif peuvent s’imbriquer dans les parties de texte d’autres \# directives if. Chaque \# directive else, \# Elif ou endif imbriquée \# appartient à la directive if précédente la plus proche \# .

Si aucune condition n’est évaluée à une valeur différente de zéro, le préprocesseur sélectionne le bloc de texte après la \# directive else. Si la \# clause else est omise et qu’aucune condition n’est évaluée à une valeur différente de zéro, aucun bloc de texte n’est sélectionné.

Les paramètres *ifCondition* et *elifCondition* répondent en grande partie aux exigences suivantes :

-   Les expressions de compilation conditionnelles sont traitées comme des valeurs [**longues signées**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) , et ces expressions sont évaluées à l’aide des mêmes règles que les expressions en C++.
-   Les expressions doivent être de type intégral et ne peuvent inclure que des constantes entières, des constantes caractère et l'opérateur defined.
-   Les expressions ne peuvent pas utiliser **sizeof** ou un opérateur de cast de type.
-   Il se peut que l'environnement cible ne puisse pas représenter toutes les plages d'entiers.
-   La traduction représente le type [**int**](/windows/desktop/WinProg/windows-data-types) identique au type **long**, et [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) identique à **unsigned long**.
-   Le traducteur peut traduire les constantes caractère en un ensemble de valeurs de code différentes de l'ensemble de l'environnement cible. Pour déterminer les propriétés de l'environnement cible, vérifiez les valeurs des macros de LIMITS.H dans une application développée pour l'environnement cible.
-   L'expression ne doit effectuer aucune interrogation de l'environnement et doit rester isolée par rapport aux détails d'implémentation sur l'ordinateur cible.

## <a name="examples"></a>Exemples

Cette section contient des exemples qui montrent comment utiliser les directives de préprocesseur de compilation conditionnelle.

### <a name="use-of-the-defined-operator"></a>Utilisation de l’opérateur défini

L’exemple suivant illustre l’utilisation de l’opérateur défini. Si le crédit d’identificateur est défini, l’appel à la fonction de **crédit** est compilé. Si le débit de l’identificateur est défini, l’appel à la fonction **Debit** est compilé. Si aucun identificateur n’est défini, l’appel à la fonction **printerror** est compilé. Notez que « CREDIT » et « Credit » sont des identificateurs distincts en C et C++, car leurs cas sont différents.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Utilisation des \# directives if imbriquées

L’exemple suivant montre comment imbriquer des \# directives if. Cet exemple suppose qu’une constante symbolique nommée DLEVEL a été définie précédemment. Les \# directives elif et \# else sont utilisées pour effectuer l’un des quatre choix, en fonction de la valeur de DLEVEL. La pile constante est définie sur 0, 100 ou 200, selon la définition de DLEVEL. Si DLEVEL est supérieur à 5, STACK n’est pas défini.


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>Utiliser pour inclure des fichiers d’en-tête

Une utilisation courante de la compilation conditionnelle consiste à empêcher plusieurs inclusions du même fichier d'en-tête. En C++, où les classes sont souvent définies dans les fichiers d’en-tête, les constructions de compilation conditionnelle peuvent être utilisées pour empêcher plusieurs définitions. L’exemple suivant détermine si l’exemple de constante symbolique \_ H est défini. Dans ce cas, le fichier a déjà été inclus et n’a pas besoin d’être retraité ; Si ce n’est pas le cas, l’exemple \_ de constante H est défini pour indiquer cet exemple. H a déjà été traité.


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

