---
title: attribut explicit_handle
description: L’attribut \ \_ CCP handle \ ACF spécifie que chaque procédure a, comme premier paramètre, un handle primitif, tel qu’un type de handle \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093609"
---
# <a name="explicit_handle-attribute"></a>\_attribut handle explicite

L' \[ attribut CCP de **\_ handle explicite** \] spécifie que chaque procédure a, en tant que premier paramètre, un handle primitif, tel qu’un type de [**handle \_ t**](handle-t.md) .

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous utilisez l’attribut **\[ \_ handle \] explicite** , chaque procédure a un handle primitif comme premier paramètre, même si le fichier IDL ne contient pas ce handle dans sa liste de paramètres. Les prototypes émis dans le fichier d’en-tête et les routines stub contiennent le paramètre supplémentaire, et ce paramètre est utilisé comme handle pour diriger l’appel distant.

L’attribut **\[ \_ handle \] explicite** affecte les procédures distantes et les procédures de sérialisation. Pour la sérialisation de type, les routines de prise en charge sont générées avec le paramètre initial en tant que handle explicite (sérialisation). Si l’attribut **\[ \_ handle \] explicite** n’est pas utilisé, l’application peut toujours spécifier qu’une opération a un handle explicite (liaison ou sérialisation) dirigeant l’appel. Pour ce faire, un prototype avec un argument contenant un type de handle est fourni au fichier IDL. Notez que, en mode par défaut, un argument qui n’apparaît pas en premier peut également être utilisé comme un handle dirigeant l’appel.

Par conséquent, si l’attribut **\[ \_ handle \] explicite** est un moyen de donner au prototype IDL un attribut de **\[ \_ handle \] explicite** primitif, il ne nécessite pas nécessairement une modification du fichier IDL. En mode [**/OSF**](-osf.md) , seul le premier argument peut être utilisé comme type de handle explicite.

L’attribut **\[ \_ handle \] explicite** peut être utilisé en tant qu’attribut d’interface ou en tant qu’attribut d’opération. En tant qu’attribut d’interface, il affecte toutes les opérations dans l’interface et tous les types qui requièrent la prise en charge de la sérialisation. Toutefois, si elle est utilisée en tant qu’attribut d’opération, elle affecte uniquement cette opération particulière. Si une méthode contient un ou plusieurs \[ \] Handles de contexte, le plus \[ à gauche dans le \] handle de contexte est utilisé comme handle de liaison, et aucun handle explicite supplémentaire n’est créé.

## <a name="examples"></a>Exemples

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




