---
title: Poignées
description: Jusqu’à deux parties dans la description de la chaîne de format d’une adresse de procédure gère.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316067"
---
# <a name="handles"></a>Poignées

Jusqu’à deux parties dans la description de la chaîne de format d’une adresse de procédure gère. La première partie est le type de handle \_<1> champ de la description d’une procédure, utilisé pour indiquer des handles implicites. Cette partie est toujours présente. La deuxième partie est une description de paramètre d’un handle explicite de la procédure. Les deux sont expliqués dans les sections suivantes, ainsi qu’une discussion de la prise en charge supplémentaire du compilateur MIDL de la structure du descripteur de stub pour les problèmes de handle de liaison.

## <a name="implicit-handles"></a>Handles implicites

Si une procédure utilise un handle implicite pour la liaison, le \_ type de handle<1> champ de la description de la procédure contient une des trois valeurs non nulles valides. La prise en charge du compilateur MIDL pour les handles implicites se trouve dans le \_ \_ champ informations de handle implicite de la structure du descripteur stub :

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

Si la procédure utilise un descripteur automatique, le membre **pAutoHandle** contient l’adresse de la variable de handle stub définie-auto.

Si la procédure utilise un handle primitif implicite, le membre **pPrimitiveHandle** contient l’adresse de la variable de handle stub définie-primitive.

Enfin, si la procédure utilise un handle générique implicite, le membre **pGenericBindingInfo** contient l’adresse du pointeur vers la structure **d' \_ \_ informations de liaison générique** correspondante. La **\_ \_ Description du stub MIDL** de la structure de données contient un pointeur vers une collection de structures de **\_ \_ paires de liaisons génériques** . L’entrée dans la position zéro de cette collection est réservée aux routines de **liaison et de** **séparation** correspondant au handle de liaison générique référencé par **pGenericBindingInfo** dans les **\_ \_ informations de handle implicites**. Le type de handle de liaison implicite est indiqué dans la chaîne de format.

## <a name="explicit-handles"></a>Handles explicites

Il existe trois types de handle explicites possibles : Context, Generic et primitive. Dans le cas d’un handle explicite (ou d’un \[  \] handle de contexte out uniquement, qui est géré de la même façon), les informations de handle de liaison s’affichent sous la forme de l’un des paramètres de la procédure. Les trois descriptions possibles sont les suivantes.

Primitives

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

L’indicateur<1> indique si le handle est passé par un pointeur.

Le décalage<2> fournit le décalage à partir du début de la pile jusqu’au handle primitif.

> [!Note]  
> Une description de handle primitif dans la chaîne de format de type est réduite à une seule valeur FC \_ ignorée.

 

Générique

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

L’indicateur \_ et la \_ taille<1> ont le grignot d’indicateur supérieur et le Quartet de la taille inférieure. L’indicateur indique si le handle est passé par un pointeur. Le champ Taille fournit la taille du type de handle générique défini par l’utilisateur. Cette taille est limitée à 1, 2 ou 4 octets sur les systèmes 32 bits et 1, 2, 4 ou 8 octets sur les systèmes 64 bits.

Le champ décalage<2> fournit le décalage à partir du début de la pile du pointeur vers les données de la taille donnée.

L' \_ \_ index de paire de routines de liaison \_<1> champ donne l’index dans le champ AGenericBindingRoutinePairs du descripteur stub aux pointeurs de fonction de **liaison** et de **détachement** de la fonction de routine pour le handle générique.

> [!Note]  
> Une description de handle générique dans le format de type est la description du type de données associé uniquement.

 

Context

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Les indicateurs<1> indiquent comment le descripteur est passé et le type. Les indicateurs valides sont indiqués dans le tableau suivant.



| Hex | Indicateur                                   |
|-----|----------------------------------------|
| 80  | le \_ paramètre handle \_ est \_ via \_ ptr            |
| 40  | le \_ paramètre \_ du handle est \_ in                  |
| 20  | le \_ paramètre de handle \_ est \_ out                 |
| 21  | le \_ paramètre handle \_ est \_ retourné              |
| 08  | \_handle de \_ contexte \_ strict NDR           |
| 04  | descripteur de contexte de NDR \_ \_ \_ non \_ Serialize    |
| 02  | désérialisation du \_ handle de contexte NDR \_ \_        |
| 01  | le \_ \_ descripteur de contexte NDR \_ ne peut pas \_ être \_ null |



 

Les quatre premiers indicateurs ont toujours été présents, les quatre derniers ont été ajoutés dans Windows 2000.

Le champ décalage<2> fournit le décalage à partir du début de la pile jusqu’au handle de contexte.

L' \_ \_ \_ index de routine d’arrêt de contexte<1> fournit un index dans le champ **apfnNdrRundownRoutines** du descripteur stub à la routine d’arrêt utilisée pour ce handle de contexte. Le compilateur génère toujours un index. Pour les routines qui n’ont pas de routine d’arrêt, il s’agit d’un index d’une position de table qui contient la valeur null.

Pour les stubs intégrés à **– Oi2**, le paramètre param \_ num<1> fournit le nombre ordinal, en commençant à zéro, en spécifiant le handle de contexte dans la procédure donnée.

Pour les versions précédentes de l’interpréteur, le \_ paramètre param num<1> fournit le numéro de paramètre du descripteur de contexte, à partir de zéro, dans sa procédure.

> [!Note]  
> Une description de handle de contexte dans la chaîne de format de type n’a pas le décalage<2> dans la description.

 

## <a name="the-new-oif-header"></a>Nouvel en-tête de l’interfaces de création

Comme mentionné précédemment, l’en-tête [**–**](/windows/desktop/Midl/-oi) de l’extension de la fonction se développe sur l’en-tête **– OI** . Pour plus de commodité, tous les champs sont affichés ici :

(L’ancien en-tête)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Les extensions de-l’extension de l' [**interfaces**](/windows/desktop/Midl/-oi) )

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

La \_ \_ taille de la mémoire tampon du client constante \_<2> fournit la taille de la mémoire tampon de marshaling qui aurait pu être précalculée par le compilateur. Il peut s’agir d’une taille partielle, car l’indicateur ClientMustSize déclenche le dimensionnement.

La \_ \_ taille de la mémoire tampon du serveur constante \_<2> fournit la taille de la mémoire tampon de marshaling telle qu’elle est précalculée par le compilateur. Il peut s’agir d’une taille partielle, car l’indicateur ServerMustSize déclenche le dimensionnement.

Les indicateurs de l’INTERPRÉTeur \_ OPT \_ sont définis dans Ndrtypes. h :

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   Le bit ServerMustSize est défini si le serveur doit effectuer une passe de dimensionnement de la mémoire tampon.
-   Le bit ClientMustSize est défini si le client doit effectuer une passe de dimensionnement de la mémoire tampon.
-   Le bit HasReturn est défini si la procédure a une valeur de retour.
-   Le bit HasPipes est défini si le package de canal doit être utilisé pour prendre en charge un argument de canal.
-   Le bit HasAsyncUuid est défini si la procédure est une procédure DCOM asynchrone.
-   Le bit HasExtensions indique que les extensions Windows 2000 et versions ultérieures sont utilisées.
-   Le bit HasAsyncHandle indique une procédure RPC asynchrone.

Le bit HasAsyncHandle a été initialement utilisé pour une implémentation DCOM différente de la prise en charge de Async et n’a donc pas pu être utilisé pour la prise en charge actuelle du style asynchrone dans DCOM. Le bit HasAsyncUuid indique actuellement cela.

 

 