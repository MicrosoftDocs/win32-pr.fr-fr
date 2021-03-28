---
title: 'RWByteAddressBuffer :: InterlockedXor, fonction'
description: Effectue un XOR atomique sur la valeur.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- InterlockedXor fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941012"
---
# <a name="interlockedxor-function"></a>InterlockedXor fonction)

Effectue un **Xor** atomique sur la valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedXor(
  in  UINT dest,
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

Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée. Il existe trois utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue un **Xor** atomique avec la valeur du registre de mémoire partagée référencé par *dest*. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue une **Xor** atomique avec la valeur de l’emplacement de la ressource référencée par *dest*. Enfin, le troisième scénario est lorsque R est un type de variable locale. Dans ce scénario, la fonction réduit à un **Xor** des valeurs de *dest* et *value*. Le résultat de l’opération remplace la valeur dans *dest*. La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de *dest*. Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| VS  | SH  | Source de données  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 