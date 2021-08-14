---
title: Descripteurs de paramètre
description: Comme mentionné précédemment, les descripteurs de paramètre de style de type d’environnement de ligne de 8211, OI et \ 8211 ; existent.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a13b052d49629333bd9cb121b4d1b661722cb3a7a69ad2a17d3e2740a0cd8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927548"
---
# <a name="parameter-descriptors"></a>Descripteurs de paramètre

Comme nous l’avons vu précédemment, les descripteurs de paramètre de style [**-OI**](/windows/desktop/Midl/-oi) et **-** de type d’environnement de ligne de fonction existent.

## <a name="the-oi-parameter-descriptors"></a>Descripteurs de paramètre – OI

Les stubs entièrement interprétés requièrent des informations supplémentaires pour chacun des paramètres d’un appel RPC. Les descriptions de paramètres d’une procédure suivent immédiatement la description de la procédure.

[**Simple – OI**](/windows/desktop/Midl/-oi)

**Descripteurs de paramètre**

Le format de la description d’un \[  \] paramètre de type simple dans ou retourne est :

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–ou–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Où le \_ type simple<1> est le jeton FC indiquant le type simple. Les codes sont les suivants :

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Autre – OI**

**Descripteurs de paramètre**

Le format de la description de tous les autres types de paramètres est le suivant :

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Où la \_ direction param<1> champ pour chacune de ces descriptions doit être l’une des valeurs indiquées dans le tableau suivant.



| Hex | Indicateur                          | Signification                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ dans \_ param                 | Paramètre in.                                            |
| 50  | Param. FC \_ en \_ sortie \_            | Paramètre in/out.                                        |
| 51  | \_paramètre de sortie FC \_                | Paramètre de sortie.                                           |
| 52  | \_param de retour FC \_             | Valeur de retour de procédure.                                   |
| 4F  | FC \_ dans \_ param \_ pas \_ d' \_ inst gratuit | Dans le port de transmission/REP en tant que paramètre pour lequel aucune libération n’est effectuée. |



 

La \_ taille de la pile<1> correspond à la taille du paramètre sur la pile, exprimée sous la forme du nombre d’entiers que le paramètre occupe sur la pile.

> [!Note]  
> Le mode [**– OI**](/windows/desktop/Midl/-oi) n’est pas pris en charge sur les plateformes 64 bits.

 

Le \_ champ décalage de type<2> est l’offset dans le type table de chaînes de format, indiquant le descripteur de type pour l’argument.

## <a name="the-oif-parameter-descriptors"></a>Descripteurs de paramètre – de l’environnement d’exécution

Il existe deux formats possibles pour une description de paramètre, un pour les types de base, un autre pour tous les autres types.

Types de base :

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

Autres :

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

Dans les deux \_ décalages de pile<2> indique le décalage sur la pile d’arguments virtuels, en octets. Pour les types de base, le type d’argument est fourni directement par le caractère de format correspondant au type. Pour les autres types, le \_ champ décalage de type<2> indique le décalage au sein de la table de chaînes de format de type où se trouve le descripteur de type de l’argument.

Le champ attribut de paramètre est défini comme suit :

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   Le bit **MustSize** est défini uniquement si le paramètre doit être dimensionné.
-   Le bit **MustFree** est défini si le serveur doit appeler la routine NdrFree du paramètre \* .
-   Le bit **IsSimpleRef** est défini pour un paramètre qui est un pointeur de référence vers tout autre pointeur, et qui n’a pas d’attribut d’allocation. Pour un tel type, l’offset de type de la description du paramètre \_<> champ, à l’exception d’un pointeur de référence vers un type de base, fournit l’offset au type du référent ; le pointeur de référence est simplement ignoré.
-   Le bit **IsDontCallFreeInst** est défini pour certains \_ paramètres, dont les routines d’instance gratuite ne doivent pas être appelées.
-   Les bits **ServerAllocSize** sont non nuls si le paramètre a la valeur \[ **out** \] , \[ **in** \] , ou \[ **in, out** pointeur \] vers le pointeur, ou pointeur vers enum16, et seront initialisés sur la pile de l’interpréteur de serveur, au lieu d’utiliser un appel à **I \_ RpcAllocate**. Si la valeur est différente de zéro, cette valeur est multipliée par 8 pour obtenir le nombre d’octets pour le paramètre. Notez que cela signifie qu’au moins 8 octets sont toujours alloués pour un pointeur.
-   Le bit **IsBasetype** est défini pour les types simples qui sont marshalés par la boucle de l’interpréteur main [**-**](/windows/desktop/Midl/-oi) out. En particulier, un type simple avec un attribut de plage sur celui-ci n’est pas marqué comme type de base afin de forcer le marshaling de routines de la routine de plage via la distribution à l’aide d’un \_ jeton de plage FC.
-   Le bit **IsByValue** est défini pour les types composés qui sont envoyés par valeur, mais n’est pas défini pour les types simples, que l’argument soit ou non un pointeur. Les types composés pour lesquels il est défini sont les structures, les unions, [**les transmissions \_ en tant que**](/windows/desktop/Midl/transmit-as) [**, le \_**](/windows/desktop/Midl/represent-as) [**\_ marshaleur de câble**](/windows/desktop/Midl/wire-marshal) et SAFEARRAY. En général, le bit a été introduit pour l’avantage de la boucle de l’interpréteur principale dans l’interpréteur [**– Oicf**](/windows/desktop/Midl/-oi) , pour s’assurer que les arguments non simples (appelés arguments de type composé) sont correctement déréférencés. Ce bit n’a jamais été utilisé dans les versions précédentes de l’interpréteur.

 

 