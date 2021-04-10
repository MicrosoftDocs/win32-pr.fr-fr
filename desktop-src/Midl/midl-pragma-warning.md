---
title: attribut midl_pragma Warning
description: Utilisez l' \_ option d’avertissement du pragma MIDL pour remplacer temporairement le comportement du message d’avertissement de MIDL au moment de la compilation.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma MIDL de l’attribut d’avertissement
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841109"
---
# <a name="midl_pragma-warning-attribute"></a>MIDL \_ pragma warning (attribut)

Utilisez l’option d' **\_ Avertissement du pragma MIDL** pour remplacer temporairement le comportement du message d’avertissement de MIDL au moment de la compilation.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*option d’avertissement \_* 
</dt> <dd>

L’option d’avertissement peut être l’une des suivantes : désactiver, activer, valeur par défaut.

</dd> <dt>

*Liste des messages \_* 
</dt> <dd>

Liste de numéros de message séparés par des espaces.

</dd> </dl>

## <a name="remarks"></a>Notes

Le pragma peut être utilisé comme un pragma de compilateur C. Autrement dit, il désactive, active ou retourne le comportement par défaut pour un avertissement MIDL donné.

## <a name="examples"></a>Exemples

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




