---
title: transmit_as (attribut)
description: L’attribut \ transmit \_ As \ demande au compilateur d’associer l’ID de type, qui est un type présenté que les applications client et serveur manipulent, avec un type de transmission de type transmis.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382829"
---
# <a name="transmit_as-attribute"></a>transmettre \_ en tant qu’attribut

L’attribut **\[ transmit \_ As \]** indique au compilateur d’associer l' **ID de type**_,_ qui est un type présenté que les applications client et serveur manipulent, avec un type de transmission de type transmis **.**

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de transmission* 
</dt> <dd>

Spécifie le type de données transmis entre le client et le serveur.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** ; attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et la chaîne d’attributs d’utilisation **\[** [](string.md) **\]** et **\[** [**ignore**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules. Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.

</dd> <dt>

*ID de type* 
</dt> <dd>

Spécifie le nom du type de données présenté aux applications clientes et serveur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour utiliser l’attribut **\[ transmettre \_ en tant que \]** , l’utilisateur doit fournir des routines qui convertissent les données entre les types présentés et transmis ; ces routines doivent également libérer de la mémoire utilisée pour stocker les données converties. L’attribut **\[ transmit \_ As \]** indique aux stubs d’appeler les routines de conversion fournies par l’utilisateur.

Le type *de* transmission de type transmis doit être résolu en un type de base MIDL, un type prédéfini ou un identificateur de type. Pour plus d’informations, consultez [types de base MIDL](midl-base-types.md).

L’utilisateur doit fournir les routines suivantes.



| Nom de la routine              | Description                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *type-ID * * * \_ à \_ transmission**   | Convertit les données du type présenté en type transmis. Cette routine alloue de la mémoire pour le type transmis et pour toutes les données référencées par des pointeurs dans le type transmis.                            |
| *ID de type * * * \_ de l' \_ émetteur** | Convertit les données du type transmis vers le type présenté. Cette routine est chargée d’allouer de la mémoire pour les données référencées par des pointeurs dans le type présenté. RPC alloue de la mémoire pour le type lui-même. |
| *ID de type * * * \_ Free \_ inst** | Libère la mémoire allouée pour les données référencées par des pointeurs dans le type présenté. RPC libère de la mémoire pour le type lui-même.                                                                                               |
| *type-ID * * * transmission \_ gratuite \_** | Libère le stockage utilisé par l’appelant pour le type transmis et pour les données référencées par des pointeurs dans le type transmis.                                                                                            |



 

 

Le stub client appelle l' *ID de type * * \_ * \_ pour* transmettre * pour allouer de l’espace pour le type transmis et pour convertir les données en objets de type transmission *-type.* Le stub serveur alloue de l’espace pour le type de données d’origine et appelle l' *ID de type * * * \_ à partir de \_* transmission * pour convertir les données de son type transmis vers le type présenté.

Lors du retour du code de l’application, le stub serveur appelle le *type-ID * * * \_ Free \_ inst** pour libérer le stockage de l' *ID de type* côté serveur. Le stub client appelle l' *ID de type * * * transmission \_ gratuite \_** pour libérer le stockage de *type* transmission côté client.

Les types suivants ne peuvent pas avoir d’attribut **\[ transmit \_ As \]** :

-   Handles de contexte (types avec l’attribut de type de **\[** [**\_ handle de contexte**](context-handle.md) **\]** et les types utilisés comme paramètres avec l’attribut de **\[ \_ handle \] de contexte** )
-   Types qui sont des canaux ou dérivés de canaux
-   Types de données utilisés comme type de base d’une définition de canal
-   Paramètres qui sont des pointeurs ou qui sont résolus en pointeurs
-   Paramètres qui sont des tableaux conformes, variables ou ouverts
-   Structures qui contiennent des tableaux conformes
-   Handle de type prédéfini [**\_ t**](handle-t.md), [**void**](void.md)

Les types transmis doivent respecter les restrictions suivantes :

-   Ils ne doivent pas être des pointeurs ou contenir des pointeurs.
-   Ils ne doivent pas être des canaux ou contenir des canaux.

## <a name="examples"></a>Exemples

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**traitée**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**nullité**](void.md)
</dt> </dl>

 

 