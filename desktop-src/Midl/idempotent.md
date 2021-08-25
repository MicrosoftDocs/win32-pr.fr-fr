---
title: idempotent (attribut)
description: L’attribut \ idempotent \ spécifie qu’une opération ne modifie pas les informations d’État et retourne les mêmes résultats chaque fois qu’elle est exécutée. L’exécution de la routine plusieurs fois a le même effet que l’exécution d’une seule fois.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- attribut idempotent MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a4135fdcb38fbad9e41b04a136f69420da7455f68d38a0c507135892e2a00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895219"
---
# <a name="idempotent-attribute"></a>idempotent (attribut)

L’attribut **\[ idempotent \]** spécifie qu’une opération ne modifie pas les informations d’État et retourne les mêmes résultats chaque fois qu’elle est exécutée. L’exécution de la routine plusieurs fois a le même effet que l’exécution d’une seule fois.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie des attributs supplémentaires à appliquer à la fonction. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut **\[ idempotent \]** sera appliqué.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Remarques

RPC prend en charge deux types de sémantiques d’appel à distance : les appels aux opérations avec l’attribut **\[ idempotent \]** et les appels aux opérations (opérations *idempotent* ) sans l’attribut **\[ idempotent \]** (opérations *non-idempotent* ). Une opération idempotent peut être exécutée plusieurs fois sans effet. À l’inverse, une opération non-idempotent ne peut pas être exécutée plus d’une fois, car elle retourne des résultats différents chaque fois ou car elle modifie un État.

Pour garantir la réexécution automatique d’une procédure si l’appel n’est pas terminé, utilisez l’attribut **\[ idempotent \]** . Si les attributs **\[ idempotent \]**, **\[** [**Broadcast**](broadcast.md) **\]** ou **\[** [**Maybe**](maybe.md) ne **\]** sont pas présents, la procédure utilise la sémantique non idempotent par défaut. Dans ce cas, l’opération n’est exécutée qu’une seule fois.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**diffusion**](broadcast.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**environ**](maybe.md)
</dt> </dl>

 

 




