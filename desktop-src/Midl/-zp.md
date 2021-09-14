---
title: /ZP (commutateur)
description: Le commutateur/ZP est le même que l’option/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- Le commutateur/ZP MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093818"
---
# <a name="zp-switch"></a>/ZP (commutateur)

Le commutateur **/ZP** est le même que l’option [**/Pack**](-pack.md) .

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*niveau de compression \_* 
</dt> <dd>

Spécifie le niveau de compression des structures dans le système cible. La valeur de niveau d’empaquetage peut être définie sur 1, 2, 4 ou 8.

</dd> </dl>

## <a name="remarks"></a>Notes

Le commutateur **/ZP** désigne le niveau de compression des structures dans le système cible. La valeur de niveau d’empaquetage correspond à la valeur de l’option **/ZP** utilisée par le compilateur Microsoft C/C++. Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++.

Spécifiez le même niveau de compression lorsque vous appelez le compilateur MIDL et le compilateur C.

Le niveau de compression par défaut utilisé lorsque le commutateur **/ZP** ou [**/Pack**](-pack.md) n’est pas spécifié est 8 dans tous les environnements de génération.

> [!Note]  
> N’utilisez pas **/Zp1** ou **/ZP2** sur des plateformes MIPS ou alpha et n’utilisez pas **/zp4** ou **/Zp8** sur les plateformes 16 bits. En fonction du type de données et de l’emplacement de mémoire attribués par le compilateur C au moment de l’exécution, cela peut entraîner une exception de non-alignement des données sur les plateformes MIPS et alpha. Sur les plateformes MS-DOS, le compilateur C ne garantit pas l’alignement à 4 ou 8, et l’application peut donc se terminer.

 

## <a name="examples"></a>Exemples

**MIDL/zp4 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> </dl>

 

 




