---
title: Descripteurs de corrélation
description: Un descripteur de corrélation est une chaîne de format qui décrit une expression basée sur un argument lié à un autre argument.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229223"
---
# <a name="correlation-descriptors"></a>Descripteurs de corrélation

Un descripteur de corrélation est une chaîne de format qui décrit une expression basée sur un argument lié à un autre argument. Un descripteur de corrélation est nécessaire pour gérer la sémantique liée à des attributs tels que la \[ **taille \_ est ()** \] , la \[ **longueur \_ est ()** \] , le \[ **commutateur \_ est ()** \] et \[ **IID \_ est ()** \] . Les descripteurs de corrélation sont utilisés avec les tableaux, les pointeurs dimensionnés, les unions et les pointeurs d’interface. La valeur de l’expression finale peut être une taille, une longueur, un discriminante d’Union ou un pointeur vers un IID, respectivement. En termes de chaînes de format, les descripteurs de corrélation sont utilisés avec les tableaux, les unions et les pointeurs d’interface. Un pointeur dimensionné est décrit dans chaînes de format en tant que pointeur vers un tableau.

Il existe deux routines effectuant des calculs d’expressions de base : NdrpComputeConformance est utilisé pour les tailles, commutateurs et IID, \* tandis que NdrpComputeVariance est utilisé pour les longueurs. Il existe également une routine unique pour effectuer une validation de valeur de corrélation pour les fonctionnalités de déni d’attaque.

Les descripteurs de corrélation ont été conçus pour prendre en charge uniquement des expressions très limitées. Pour les situations complexes, le compilateur génère une routine d’évaluation d’expression qui doit être appelée par le moteur quand cela est nécessaire.

Un descripteur de corrélation a le format suivant :

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

Le type de corrélation du descripteur \_ de corrélation<1> se compose de deux quartets : les 4 bits de poids fort décrivent où l’expression peut être trouvée et les 4 bits inférieurs décrivent le type de la valeur de l’expression.

Le Quartet supérieur peut avoir l’une des cinq valeurs suivantes :

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformité normale \_ FC
</dt> <dd>

Une situation normale de conformité, telle que celle décrite dans un champ d’une structure.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformité du pointeur FC \_
</dt> <dd>

Pour les pointeurs avec attributs (la **taille \_ est ()**, la **longueur \_ est ()**) qui sont des champs dans une structure. Cela affecte la façon dont le pointeur de la mémoire de base est défini.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_ \_ conformité au niveau supérieur FC \_
</dt> <dd>

Pour la conformité de niveau supérieur décrite par un autre paramètre.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformité multithread à niveau supérieur \_ FC \_
</dt> <dd>

Pour la conformité de niveau supérieur d’un tableau multidimensionnel décrit par un autre paramètre.

> [!Note]  
> Les pointeurs et les tableaux de taille multidimensionnelle déclenchent un commutateur à [**– Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMITÉ de la \_ constante FC \_
</dt> <dd>

Pour une valeur constante. Le compilateur Précalcule la valeur à partir d’une expression constante fournie par l’utilisateur. Dans ce cas, les 3 octets suivants dans la description de conformité contiennent les 3 octets inférieurs d’une longue qui décrivent la taille de la conformité. Aucun calcul supplémentaire n’est nécessaire.

</dd> </dl>

Le Quartet inférieur donne le type de la valeur qui doit être extraite de la mémoire :

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> les expressions 64 bits ne sont pas prises en charge. FC \_ hyper est utilisé uniquement pour **IID \_ est ()** sur les plateformes 64 bits pour extraire la valeur de pointeur pour IID \* .
>
> Le compilateur définit le Quartet de type sur zéro dans les cas suivants : expression constante mentionnée ci-dessus et lorsque la routine d’expression d’évaluation doit être appelée, par exemple, lorsque la conformité à la \_ constante FC \_ et le \_ rappel FC sont utilisés.

 

La taille \_ est le \_ champ op<1> permet d’appliquer l’une des opérations suivantes à la variable de conformité :

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

La \_ constante de DÉréférencement FC est utilisée pour que la corrélation soit un point, comme pour la **\[ taille \_ est ( \* pl) \]**. Les opérateurs arithmétiques utilisent simplement la constante indiquée. La \_ constante de rappel FC indique qu’une routine d’évaluation de l’expression doit être appelée.

Le champ décalage<2> correspond généralement à un décalage de mémoire relatif à la variable d’argument expression. Il peut également s’agir d’une évaluation d’expression – index de routine. Comme mentionné précédemment dans ce document, pour les expressions constantes, il fait partie de la valeur de l’expression finale réelle.

L’interprétation du champ offset<2> en tant que décalage de la mémoire dépend de la complexité de l’expression, de l’emplacement de la variable d’expression et, dans le cas d’un tableau, du fait que le tableau est effectivement un pointeur avec attributs.

Si le tableau est un pointeur avec attributs et que la variable de conformité est un champ dans une structure, le champ de décalage contient le décalage entre le début de la structure et le champ de description de la conformité. Si le tableau n’est pas un pointeur attribué et que la variable de conformité est un champ dans une structure, le champ de décalage contient le décalage entre la fin de la partie non conforme de la structure et le champ de description de la conformité. En règle générale, le tableau conforme se trouve à la fin de la structure.

Pour la conformité de niveau supérieur, le champ de décalage contient le décalage à partir de l’emplacement du premier paramètre du stub sur la pile jusqu’au paramètre qui décrit la conformité. Cela n’est pas utilisé en mode **– système d’exploitation** . Il existe d’autres exceptions à l’interprétation du champ de décalage ; de telles exceptions sont décrites dans la description de ces types.

Lorsque l’offset<2> est utilisé avec \_ le rappel FC, il contient un index dans la table de routine d’évaluation d’expression générée par le compilateur. Le message stub est passé à la routine d’évaluation, qui calcule ensuite la valeur de conformité et l’assigne au champ MaxCount du message stub.

le \_ champ indicateurs robustes<2> a été ajouté pour Windows 2000 afin de prendre en charge [**/robust**](/windows/desktop/Midl/-robust), par exemple la fonctionnalité de refus d’attaques. Les indicateurs suivants sont définis sur le premier octet :

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

L’indicateur précoce indique une corrélation précoce et tardive. Une corrélation précoce est lorsque l’argument expression précède l’argument décrit, par exemple un argument de taille est avant un argument de pointeur de taille. Une corrélation tardive est lorsque l’argument d’expression vient après l’argument associé. Le moteur effectue immédiatement la validation des valeurs de corrélation précoces, les valeurs de corrélation tardives sont stockées pour vérification une fois le démarshaling effectué.

L’indicateur Split indique un fractionnement asynchrone entre les \[ \] arguments in et \[ out \] . Par exemple, un argument de taille peut être \[ dans \] alors que le pointeur dimensionné peut être en \[ sortie \] . Dans le contexte asynchrone DCOM, ces arguments se trouvent sur des piles différentes ; le moteur doit donc en être conscient.

L’indicateur IsIidIs indique que la corrélation **IID \_ est ()** . La routine NdrComputeConformance est confrontée à l’obtention d’un pointeur vers IID en tant que valeur d’expression, mais la routine de validation ne peut pas comparer ces valeurs (il s’agit de pointeurs) et l’indicateur indique donc que les IID réels doivent être comparés.

### <a name="variance-description-and-other-array-attributes"></a>Description de l’écart et autres attributs du tableau

Le format du champ Description de l’écart est identique au champ Description de la conformité. La différence réside dans le fait qu’un autre champ de message stub est utilisé par le moteur de NDR comme une variable temporaire. Dans le cas de la description de l’écart, il s’agit de la longueur qui est évaluée et le champ correspondant est appelé ActualLength.

Avec la variance, le décalage de départ est généralement égal à zéro et le moteur est réglé en conséquence. Si le **premier attribut \_ est ()** est appliqué à un tableau variable conforme, un rappel à une routine d’évaluation d’expression est forcé.

 

 