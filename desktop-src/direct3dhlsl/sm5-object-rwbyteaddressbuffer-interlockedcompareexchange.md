---
title: 'RWByteAddressBuffer :: InterlockedCompareExchange, fonction'
description: Compare l’entrée à la valeur de comparaison et échange le résultat, de manière atomique.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- InterlockedCompareExchange fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729141"
---
# <a name="interlockedcompareexchange-function"></a>InterlockedCompareExchange fonction)

Compare l’entrée à la valeur de comparaison et échange le résultat, de manière atomique.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*dest* \[ . dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Adresse de destination.

</dd> <dt>

*comparer la \_ valeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valeur de comparaison.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valeur d'entrée.

</dd> <dt>

*\_ valeur d’origine* \[\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valeur d'origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Compare atomiquement la valeur de *dest* à *la \_ valeur de comparaison*, stocke la valeur dans *dest* si les valeurs correspondent, retourne la valeur d’origine de *dest* dans la *\_ valeur d’origine*. Cette opération ne peut être effectuée que sur des ressources typées **int** ou *uint* et des variables de mémoire partagée. Il existe trois utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*. Enfin, le troisième scénario est lorsque R est un type de variable locale. Dans ce scénario, la fonction réduit à l’opération effectuée à l’aide d’opérations locales. Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.

> [!Note]  
> Si vous appelez **InterlockedCompareExchange** dans une boucle de nuanceur [**de calcul for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) , pour compiler correctement, vous devez utiliser l’attribut de **\[ \_ \_ \] condition allow UAV** sur cette boucle.

 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| VS  | SH  | Source de données  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 