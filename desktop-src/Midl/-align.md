---
title: commutateur/align
description: Le commutateur/align est fonctionnellement identique à l’option/ZP/ZP et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- MIDL du commutateur/align
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093981"
---
# <a name="align-switch"></a>commutateur/align

Le commutateur **/align** est fonctionnellement identique à l’option [**/ZP/ZP**](-zp.md) et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec mktyplib.

> [!Note]  
> L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*repère* 
</dt> <dd>

Spécifie l’alignement pour les types dans la bibliothèque. La valeur d' *alignement* peut être 1, 2, 4 ou 8. La valeur 1 indique l’alignement naturel ; *n* indique l’alignement sur l’octet *n*. Si vous ne spécifiez pas le commutateur **/align** , la valeur par défaut est 8.

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous générez un nouveau Makefile, utilisez le commutateur [**/ZP**](-zp.md) .

La valeur d’alignement correspond à la valeur de l’option [**/ZP**](-zp.md) utilisée par le compilateur Microsoft C/C++. Veillez à spécifier le même alignement lorsque vous appelez le compilateur C comme lorsque vous appelez le compilateur MIDL.

Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++. Pour plus d’informations sur les risques potentiels liés à l’utilisation de niveaux de compression non standard, consultez la rubrique d’aide [**/ZP**](-zp.md) .

## <a name="examples"></a>Exemples

**MIDL/align : 4 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




