---
title: async_uuid (attribut)
description: L’attribut \ Async \_ UUID \ interface indique au compilateur MIDL de définir à la fois les versions synchrones et asynchrones d’une interface com.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid MIDL de l’attribut
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fd7b4d9d9bf7a595415e55de778a419d91051c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093781"
---
# <a name="async_uuid-attribute"></a>\_attribut UUID Async

L’attribut d’interface **\[ \_ UUID \] Async** indique au compilateur MIDL de définir à la fois les versions synchrones et asynchrones d’une interface com.

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*chaîne uuid1* 
</dt> <dd>

Chaîne UUID, générée par l’utilitaire uuidgen, qui identifie la version synchrone de l’interface.

</dd> <dt>

*chaîne uuid2* 
</dt> <dd>

Chaîne UUID, générée par l’utilitaire uuidgen, qui identifie la version asynchrone de l’interface.

</dd> <dt>

*interface-attribut-List* 
</dt> <dd>

Autres attributs qui s’appliquent à l’ensemble de l’interface. Vous ne pouvez pas utiliser l’attribut [**\[ version \]**](version.md) dans une interface com.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface.

</dd> <dt>

*interface de base* 
</dt> <dd>

Interface à partir de laquelle cette interface dérive. L’interface de base doit être **IUnknown** ou une interface asynchrone qui dérive, directement ou indirectement, de **IUnknown**.

</dd> <dt>

*définition d’interface* 
</dt> <dd>

Spécifie les instructions IDL qui forment la définition de l’interface.

</dd> </dl>

## <a name="remarks"></a>Notes

l’utilisation de cet attribut requiert Windows versions 2000 ou ultérieures de Windows.

Lorsque vous appliquez l’attribut **\[ \_ UUID \] Async** à une interface com (autrement dit, une interface qui a l’attribut [**\[ objet \]**](object.md) ), le compilateur MIDL génère une définition asynchrone de l’interface, en plus de la version synchrone traditionnelle. L’interface asynchrone aura les mêmes noms que l’interface synchrone, mais avec un préfixe « Async ». L’identificateur d’interface (IID) est l’UUID spécifié en tant que paramètre de l’attribut **\[ \_ UUID \] Async** .

Pour l’interface asynchrone, MIDL fractionne chaque méthode en méthodes de *début* et de *fin* distinctes. La méthode *Begin* a le nom de la méthode synchrone avec un \_ préfixe « Begin » et inclut tous les paramètres [**\[ in \]**](in.md) de la méthode synchrone. La méthode *Finish* a le nom de la méthode synchrone avec un \_ préfixe « Finish » et inclut tous les paramètres [**\[ out \]**](out-idl.md) de la méthode synchrone. Si la méthode synchrone possède des paramètres **\[ in, \] out,** ils sont inclus dans les méthodes asynchrones *Begin* et *Finish* .

Si une méthode d’interface asynchrone a l' [**\[ appel \_ en tant qu' \]**](call-as.md) attribut, MIDL génère des déclarations pour les méthodes *Begin* et *Finish* . Vous devez implémenter les deux méthodes.

Chaque interface asynchrone est un modificateur sur une interface synchrone et, par conséquent, n’a pas de graphique d’héritage distinct. Cela signifie que vous ne pouvez pas définir une interface synchrone à partir d’une interface asynchrone (autre que **IUnknown**). Les interfaces synchrones et ne peuvent pas non plus hériter d’interfaces asynchrones. Le compilateur MIDL émet un message d’erreur si vous tentez l’un ou l’autre.

## <a name="examples"></a>Exemples

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définition d’interfaces COM](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**appeler \_ en tant que**](call-as.md)
</dt> <dt>

[**IID \_ est**](iid-is.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 