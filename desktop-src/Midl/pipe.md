---
title: attribut de canal
description: Le constructeur de type pipe permet de transmettre un flux ouvert de données typées à travers un appel de procédure distante.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- MIDL (MIDL), attribut de canal
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314760"
---
# <a name="pipe-attribute"></a>attribut de canal

Le constructeur de type **pipe** permet de transmettre un flux ouvert de données typées à travers un appel de procédure distante.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type d’élément* 
</dt> <dd>

Définit la taille d’un élément unique dans la mémoire tampon de transfert. Le type d' *élément* peut être un [type de base](midl-base-types.md), un type prédéfini \_ , un [**struct**](struct.md), une [**énumération 32b**](v1-enum.md)ou un identificateur de type. Plusieurs restrictions s’appliquent aux *\_ types d’éléments*, comme décrit dans la section Notes ci-dessous.

</dd> <dt>

*canal-déclarateur* 
</dt> <dd>

Spécifie un ou plusieurs identificateurs ou pointeurs vers des identificateurs. Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser le constructeur de type **pipe** pour transmettre des données dans les deux sens. Un **\[** [](in.md) **\]** paramètre in pipe permet au serveur d’extraire le flux de données du client pendant un appel de procédure distante. Un **\[** paramètre de [**sortie**](out-idl.md) de **\]** canal permet au serveur d’envoyer à nouveau le flux de données au client. Vous fournissez les routines côté client pour l’envoi et l’extraction du flux de données et pour allouer une mémoire tampon globale pour les données. Les routines de stub client et serveur marshalent et démarshalent les données et transmettent une référence à la mémoire tampon à l’application.

Les restrictions suivantes s’appliquent aux canaux :

-   Un élément pipe ne peut pas être ou contenir un pointeur, un tableau conforme ou variable, un handle ou un handle de contexte. En outre, dans l’implémentation Microsoft des canaux, un élément pipe ne peut pas être ou contenir une [**Union**](union.md), une [**énumération 16B**](enum.md)ou un [**\_ \_ int3264**](--int3264.md).
-   Vous ne pouvez pas appliquer les **\[** attributs de [**transmission \_ en tant que**](transmit-as.md) **\]** , de marshaling en tant que, **\[** [**\_**](represent-as.md) **\]** **\[** de [**\_ marshaling de câble**](wire-marshal.md)ou de **\]** **\[** [**\_ Marshal utilisateur**](user-marshal.md) **\]** à un type de canal ou au *type d’élément*.
-   Un type de canal ne peut pas être un membre d’une structure ou d’une Union, la cible d’un pointeur ou le type de base d’un tableau.
-   Un type de données déclaré comme étant un type de canal ne peut être utilisé qu’en tant que paramètre d’un appel distant.
-   Vous pouvez passer un paramètre de canal dans l’une ou l’autre direction par valeur ou par référence ( **\[** pointeur [**ref**](ref.md) **\]** ). Toutefois, vous ne pouvez pas appliquer l' **\[** [](ptr.md) **\]** attribut PTR à un canal qui est passé par référence. Vous ne pouvez pas spécifier un paramètre de canal avec un **\[** [](unique.md) **\]** pointeur unique ou complet, quelle que soit la direction.
-   Vous ne pouvez pas utiliser de canaux dans des interfaces d' **\[** [**objet**](object.md) **\]** .
-   Vous ne pouvez pas appliquer l' **\[** [](idempotent.md) **\]** attribut idempotent à une routine qui a un paramètre pipe.
-   Vous ne pouvez pas utiliser les attributs de sérialisation, **\[** [**Encoder**](encode.md) **\]** et **\[** [**décoder**](decode.md) **\]** avec des canaux.
-   Vous ne pouvez pas utiliser de handles automatiques, par défaut, ou avec l’attribut de **\[** [**\_ gestion automatique**](auto-handle.md) **\]** , avec des canaux.

> [!Note]  
> Le compilateur MIDL prend en charge les canaux en mode [**/OIF**](-oi.md) uniquement.

 

Pour plus d’informations sur l’implémentation des routines avec des paramètres de canal, consultez [canaux](/windows/desktop/Rpc/pipes) dans le Guide du programmeur RPC et référence.

## <a name="examples"></a>Exemples

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**décoder**](decode.md)
</dt> <dt>

[**contraire**](encode.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**représenter \_ comme**](represent-as.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**Marshal d’utilisateur \_**](user-marshal.md)
</dt> <dt>

[**Marshal de câble \_**](wire-marshal.md)
</dt> </dl>

 

 