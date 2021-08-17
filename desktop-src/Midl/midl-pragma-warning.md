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
ms.openlocfilehash: 0ae8e902d1e58ff216f36ae8003dc8f3f553a32005136ef2a86201bd17279107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067089"
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

## <a name="remarks"></a>Remarques

Le pragma peut être utilisé comme un pragma de compilateur C. Autrement dit, il désactive, active ou retourne le comportement par défaut pour un avertissement MIDL donné.

## <a name="examples"></a>Exemples

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Bali**](pragma.md)
</dt> </dl>

 

 




