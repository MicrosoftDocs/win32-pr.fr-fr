---
title: mot clé Union (RPC)
description: Les unions requièrent des mots clés MIDL spéciaux pour prendre en charge leur utilisation avec l’appel de procédure distante (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011387"
---
# <a name="union-keyword-rpc"></a>mot clé Union (RPC)

Certaines fonctionnalités du langage C, telles que les unions, requièrent des mots clés MIDL spéciaux pour prendre en charge leur utilisation dans les appels de procédure distante. Une Union dans le langage C est une variable qui contient des objets de différents types et tailles. Le développeur crée généralement une variable pour effectuer le suivi des types stockés dans l’Union. Pour fonctionner correctement dans un environnement distribué, la variable qui indique le type de l’Union, ou *discriminante*, doit également être disponible pour l’ordinateur distant. MIDL fournit le \[ [**\_ type de commutateur**](/windows/desktop/Midl/switch-type) \] et le \[ [**commutateur \_ est**](/windows/desktop/Midl/switch-is) un \] mot clé pour identifier le type et le nom discriminante.

MIDL exige que le discriminante soit transmis avec l’Union de deux manières :

-   L’Union et le discriminante doivent être fournis en tant que paramètres.
-   L’Union et le discriminante doivent être empaquetés dans une structure.

Deux types fondamentaux d’unions discriminées sont fournis par MIDL : [**\_ Union**](/windows/desktop/Midl/nonencapsulated-unions) et [**\_ Union encapsulée**](/windows/desktop/Midl/encapsulated-unions). Le discriminante d’une Union non encapsulée est un autre paramètre si l’Union est un paramètre. Il s’agit d’un autre champ si l’Union est un champ d’une structure. La définition d’une Union encapsulée est transformée en définition de structure dont le premier champ est le discriminante et dont le deuxième et le dernier champs sont l’Union. L’exemple suivant montre comment fournir les paramètres Union et discriminante :

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

Dans l’exemple précédent, l’Union peut contenir une valeur unique : **short**, **float** ou **char**. La définition de type pour l’Union comprend l’attribut de **\_ type de commutateur** MIDL qui spécifie le type de discriminante. Ici, \[ \_ type de commutateur (short) \] spécifie que le discriminante est de type **short**. Le commutateur doit être un type entier.

Si l’Union est un membre d’une structure, discriminante doit être un membre de la même structure. Si l’Union est un paramètre, discriminante doit être un autre paramètre. Le prototype de la fonction **UnionParamProc** dans l’exemple précédent montre le *sUtype* discriminante en tant que dernier paramètre de l’appel. (Le discriminante peut apparaître à n’importe quelle position dans l’appel.) Le type du paramètre spécifié dans le **\[ commutateur \_ est \]** attribute doit correspondre au type spécifié dans l’attribut de **\[ \_ type \] de commutateur** .

L’exemple suivant illustre l’utilisation d’une structure unique qui empaquette le discriminante avec l’Union :

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Le compilateur Microsoft RPC MIDL autorise les déclarations d’Union en dehors des constructions [**typedef**](/windows/desktop/Midl/typedef) . Cette fonctionnalité est une extension de l’IDL DCE. Pour plus d’informations, consultez [**Union**](/windows/desktop/Midl/union).

 

 