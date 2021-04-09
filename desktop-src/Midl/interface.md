---
title: interface (attribut)
description: Le mot clé interface spécifie le nom de l’interface. Le nom de l’interface doit être fourni à la fois dans le fichier IDL et dans le CCP.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- MIDL, attribut d’interface
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842157"
---
# <a name="interface-attribute"></a>interface (attribut)

Le mot clé **interface** spécifie le nom de l’interface. Le nom de l’interface doit être fourni à la fois dans le fichier IDL et dans le CCP.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie des attributs qui s’appliquent à l’ensemble de l’interface. Les attributs d’interface valides pour un fichier IDL incluent le **\[** [**point de terminaison**](endpoint.md) **\]** , l' **\[** objet [**local**](local.md) **\]** , l' **\[** [**objet**](object.md) **\]** , le **\[** [**pointeur \_ par défaut**](pointer-default.md) **\]** , l' **\[** [**UUID**](uuid.md) **\]** et la **\[** [**version**](version.md) **\]** . Les attributs d’interface valides pour un CCP incluent l' **\[** [**encodage**](encode.md) **\]** , le **\[** [**décodage**](decode.md) **\]** , le **\[** [**\_ handle automatique**](auto-handle.md) **\]** ou le **\[** [**\_ handle implicite**](implicit-handle.md) **\]** , ainsi que le **\[** [**code**](code.md) **\]** ou le **\[** [**nocode**](nocode.md) **\]** .

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface. Le nom de l’interface doit être un nom unique et doit commencer par un caractère alphabétique ou un trait de soulignement.

</dd> <dt>

*interface de base* 
</dt> <dd>

Spécifie le nom d’une interface à partir de laquelle cette interface dérivée hérite des fonctions membres, des codes d’État et des attributs d’interface. L’interface dérivée n’hérite pas des définitions de type. Pour ce faire, utilisez le mot clé [**Import**](import.md) pour importer le fichier IDL de l’interface de base.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Les noms d’interface dans le fichier IDL et ACF doivent être identiques, sauf lorsque vous utilisez le commutateur du compilateur MIDL [**/ACF**](-acf.md).

Le nom d’interface constitue la première partie du nom des structures de données de handle d’interface qui sont des paramètres pour les fonctions runtime RPC. Pour plus d’informations, consultez [**RPC \_ if \_ descripteur**](/windows/desktop/Rpc/rpc-if-handle).

Si l’en-tête d’interface inclut l' **\[** [](object.md) **\]** attribut d’objet pour indiquer une interface com, il doit également inclure l' **\[** attribut [**UUID**](uuid.md) **\]** et doit spécifier l’interface com de base à partir de laquelle elle est dérivée. Pour plus d’informations sur les interfaces COM, consultez **\[** [**objet**](object.md) **\]** .

Vous pouvez également utiliser le mot clé **interface** avec le mot clé [**typedef**](typedef.md) pour définir un type de données d’interface.

## <a name="examples"></a>Exemples

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**pointeur \_ par défaut**](pointer-default.md)
</dt> <dt>

[**\_handle RPC if \_**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 