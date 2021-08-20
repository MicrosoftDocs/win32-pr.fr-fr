---
title: attribut handle_t
description: Le \_ mot clé handle t déclare un objet comme étant du handle de type de handle primitif \_ t. Un handle de liaison primitif est un objet de données qui peut être utilisé par l’application pour représenter la liaison.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a2574908891d29baf9d4748943d0550f3f015eddccbdd123e31598b39b08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991327"
---
# <a name="handle_t-attribute"></a>handle \_ t (attribut)

Le mot clé **handle \_ t** déclare un objet comme étant du handle de type de handle primitif **\_ t**. Un handle de liaison primitif est un objet de données qui peut être utilisé par l’application pour représenter la liaison.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Paramètres

Cet attribut n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Le type de **handle \_ t** est l’un des types prédéfinis du langage IDL (Interface Definition Language). Il peut apparaître comme un spécificateur de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

Dans Microsoft RPC, les paramètres de type **handle \_ t** peuvent se produire uniquement comme **\[** paramètres [**in**](in.md) **\]** . Les handles primitifs ne peuvent pas avoir l' **\[** attribut [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** .

Les paramètres de type **handle \_ t** (paramètres de handle primitifs) ne sont pas transmis sur le réseau.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[Liaison et Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 