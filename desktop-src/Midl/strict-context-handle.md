---
title: attribut strict_context_handle
description: L’attribut \ \_ \_ ACF du handle de contexte \ CCP définit des restrictions sur les handles de contexte.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013577"
---
# <a name="strict_context_handle-attribute"></a>attribut de handle de \_ contexte strict \_

Le **\[ strict \_ \_ handle \] de contexte** CCP définit des restrictions sur les handles de contexte.

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Autres attributs ACF qui s’appliquent à l’ensemble de l’interface. Les attributs valides incluent le [**\_ descripteur automatique**](auto-handle.md), le [**\_ handle implicite**](implicit-handle.md), le [**\_ handle explicite**](explicit-handle.md)et l' [**optimisation**](optimize.md), le [**code**](code.md)ou le [**nocode**](nocode.md). Séparez plusieurs attributs par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface.

</dd> <dt>

*interface-définition-instructions* 
</dt> <dd>

Une ou plusieurs instructions MIDL qui définissent les éléments de l' [**interface**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Normalement, lorsqu’un appel à une méthode d’interface génère un handle de contexte, ce descripteur devient librement disponible pour toute autre interface. Lorsque vous utilisez l’attribut de **\[ \_ \_ handle \] de contexte strict** , vous garantissez que les méthodes de cette interface acceptent uniquement les handles de contexte qui ont été créés par une méthode à partir de la même interface. Les interfaces compilées sans un **\[ \_ \_ handle \] de contexte strict** ne peuvent pas accepter des handles de contexte créés sur des interfaces compilées avec un **\[ \_ \_ \] handle de contexte strict**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**code**](code.md)
</dt> <dt>

[Handles de contexte](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_sérialisation du handle de contexte \_**](context-handle-serialize.md)
</dt> <dt>

[**handle de contexte \_ \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**\_handle explicite**](explicit-handle.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> <dt>

[**requêtes**](optimize.md)
</dt> <dt>

[\_handle de \_ contexte \_ strict de type](type-strict-context-handle.md)
</dt> </dl>

 

 