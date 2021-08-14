---
title: Allocate (attribut)
description: L’attribut \ Allocate \ ACF vous permet de personnaliser l’allocation et la désallocation de mémoire pour un type défini dans le fichier IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- MIDL de l’attribut Allocate
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345652b9da5ed5087793606d963d6cf9b8ce225587ee150c27f6410ae99b8d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808436"
---
# <a name="allocate-attribute"></a>Allocate (attribut)

L’attribut **\[ allocate \]** ACF vous permet de personnaliser l’allocation et la désallocation de mémoire pour un type défini dans le fichier IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*allocate-option-list* 
</dt> <dd>

Spécifie une ou plusieurs options d’allocation de mémoire. Sélectionnez l’un des nœuds **uniques \_** ou **tous les \_ nœuds**, ou l’un des deux, **gratuit** ou non, ou un de chaque paire. **\_** Lorsque vous spécifiez plusieurs options, séparez-les par des virgules.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs CCP-type facultatifs. Lorsque vous spécifiez plusieurs attributs de type, séparez les options par des virgules.

</dd> <dt>

*nom du type* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’attribut **\[ allocate \]** a les options valides suivantes.



| Option           | Description                                                           |
|------------------|-----------------------------------------------------------------------|
| **tous les \_ nœuds**   | Effectue un appel pour allouer et libérer de la mémoire pour tous les nœuds.             |
| **\_nœud unique** | Effectue de nombreux appels individuels pour allouer et libérer chaque nœud de mémoire. |
| **free**         | Libère de la mémoire au retour du stub serveur.                          |
| **ne pas \_ libérer**   | Ne libère pas de mémoire au retour du stub serveur.                  |



 

Par défaut, les stubs peuvent allouer du stockage pour les données référencées par un pointeur unique ou complet en appelant [**MIDL \_ User \_ allocate**](midl-user-allocate-1.md) et [**MIDL \_ User \_ Free**](midl-user-free-1.md) individuellement pour chaque pointeur.

Vous pouvez optimiser la vitesse de votre application en spécifiant l’option **tous les \_ nœuds**. Cette option indique au stub de calculer la taille de la mémoire référencée par le pointeur du type spécifié et d’effectuer un appel unique à l' [**\_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md). Le stub libère la mémoire en effectuant un appel à l' [**\_ utilisateur MIDL \_ gratuit**](midl-user-free-1.md).

L’option **ne pas \_ libérer** indique au compilateur MIDL de générer un stub de serveur qui n’appelle pas l' [**\_ utilisateur MIDL \_ gratuit**](midl-user-free-1.md) pour le type spécifié. L’option **ne pas \_ libérer** permet aux structures de pointeur de rester accessibles à l’application serveur une fois que l’appel de procédure distante est terminé et retourné au client.

L’attribut **\[ allocate \]** entraîne un paramètre **\[ in \] , out** qui est un pointeur vers un type qualifié avec l’option **All \_ Nodes** pour réallouer de la mémoire lorsque les données sont démarshalées. Il est de la responsabilité de l’application de libérer la mémoire allouée précédemment pour ce paramètre. Par exemple :

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

Le type de données PTHISTYPE sera réalloué dans le sens de [**\[ sortie \]**](out-idl.md) par le stub avant d’être démarshalé. Par conséquent, l’application doit libérer la mémoire qu’elle avait allouée précédemment pour les données de ce paramètre, ou une fuite de mémoire se produira.

## <a name="examples"></a>Exemples

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**allouer un \_ utilisateur MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**\_utilisateur \_ gratuit MIDL**](midl-user-free-1.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




