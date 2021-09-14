---
title: typedef (attribut)
description: Le mot clé IDL IDL autorise les déclarations typedef qui sont très similaires aux déclarations typedef du langage C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- MIDL de l’attribut typedef
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093105"
---
# <a name="typedef-attribute"></a>typedef (attribut)

Le mot **clé** IDL IDL autorise les déclarations **typedef** qui sont très similaires aux déclarations **typedef** du langage C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*IDL-type-attribute-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides dans un fichier IDL incluent **\[** [**descripteur**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*. Le mot clé [**const**](const.md) peut précéder le *type-specifier*.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs MIDL standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.

</dd> <dt>

*ACF-type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Les attributs de type valides dans un CCP incluent l' **\[** [**allocation**](allocate.md) **\]** , l' **\[** [**encodage**](encode.md) **\]** et le **\[** [**décodage**](decode.md) **\]** .

</dd> <dt>

*TypeName* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

La déclaration de **typedef** IDL est augmentée pour vous permettre d’associer des attributs de type aux types définis. Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .

Le mot clé **typedef** dans un ACF applique des attributs aux types définis dans le fichier IDL correspondant. Par exemple, l’attribut [**allocate**](allocate.md) type vous permet de personnaliser l’allocation et la désallocation de mémoire à la fois par l’application et les stubs.

L’instruction de **typedef** ACF s’affiche dans le corps du CCP. Notez que la syntaxe du **typedef** ACF est différente de la **syntaxe du typedef IDL et** de la syntaxe **typedef** du langage C. Aucun nouveau type ne peut être introduit dans le CCP.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**décoder**](decode.md)
</dt> <dt>

[**contraire**](encode.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**traitée**](handle.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignore**](ignore.md)
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

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 