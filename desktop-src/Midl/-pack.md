---
title: commutateur/Pack
description: Le commutateur/Pack est le même que l’option/zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL du commutateur/Pack
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9282cd5ab56d2e037ba585676a83c5cd558ecb26354ab191899ad341506f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991941"
---
# <a name="pack-switch"></a>commutateur/Pack

Le commutateur **/Pack** est le même que l’option [**/ZP**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*niveau de compression \_* 
</dt> <dd>

Spécifie le niveau de compression des structures dans le système cible. La valeur de niveau d’empaquetage peut être définie sur 1, 2, 4 ou 8.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le commutateur **/Pack** désigne le niveau de compression des structures dans le système cible. La valeur de niveau d’empaquetage correspond à la valeur de l’option [**/ZP**](-zp.md) utilisée par le compilateur Microsoft C/C++ version 7,0. Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++.

Spécifiez le même niveau de compression lorsque vous appelez le compilateur MIDL et le compilateur C. Le niveau de compression par défaut utilisé lorsque le commutateur [**/ZP**](-zp.md) ou **/Pack** n’est pas spécifié est 8, dans tous les environnements de génération.

Pour plus d’informations sur les risques potentiels liés à l’utilisation de niveaux de compression non standard, consultez la rubrique d’aide [**/ZP**](-zp.md) .

## <a name="examples"></a>Exemples

**MIDL/Pack 2 nom de fichier. idl**

**MIDL/Pack 8 bar. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




