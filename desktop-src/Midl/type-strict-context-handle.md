---
title: attribut type_strict_context_handle
description: Utilisez le gestionnaire de \_ contexte \ type strict \_ \_ \ dans un fichier ACF pour définir des restrictions sur les handles de contexte.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462982"
---
# <a name="type_strict_context_handle-attribute"></a>\_attribut de \_ handle de contexte strict \_

Utilisez le **\[ type \_ strict \_ \_ handle \] de contexte** dans un fichier ACF pour définir des restrictions sur les handles de contexte.

``` syntax
[ 
    type_strict_context_handle 
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

## <a name="remarks"></a>Notes

Pour pouvoir utiliser cet attribut, l’indicateur-target doit avoir la valeur NT60 (ou une version ultérieure) lors de l’exécution de midl.exe.

\[\_le type \_ \_ de handle de contexte strict \] est un sur-ensemble fonctionnel du \[ handle de \_ contexte strict \_ \] . Dans \[ \_ un handle de contexte strict \_ \] , l’ID de type du descripteur est toujours 0 ; dans \[ le type de \_ handle de \_ contexte strict \_ \] , un ID de type unique est assigné par le compilateur MIDL.

Il est recommandé d’utiliser \[ un \_ \_ handle de contexte strict \_ \] plutôt qu’un \[ handle de contexte strict \_ \_ \] . Les handles de contexte ne sont pas associés à un type spécifique par défaut. Lorsque plusieurs types de handles de contexte sont utilisés dans le même processus, un client malveillant peut passer un handle de contexte à la place d’un autre pour produire des résultats indésirables. L’utilisation du \[ \_ handle de \_ contexte \_ strict \] permet aux applications d’appliquer la cohérence des types de handles de contexte et d’empêcher toute utilisation incompatible de type de handle de contexte.

Un handle de contexte attribué avec un \[ handle de contexte de type \_ strict \_ \_ \] ne peut pas également être attribué avec un \[ handle de \_ contexte strict \_ \] .

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

[\_handle de contexte strict \_](strict-context-handle.md)
</dt> </dl>

 

 