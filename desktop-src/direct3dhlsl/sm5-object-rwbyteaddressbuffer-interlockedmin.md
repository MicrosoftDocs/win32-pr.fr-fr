---
title: 'RWByteAddressBuffer :: InterlockedMin, fonction'
description: Recherche la valeur minimale, atomiquement.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031262"
---
# <a name="interlockedmin-function"></a>InterlockedMin fonction)

Recherche la valeur minimale, atomiquement.

## <a name="syntax"></a>Syntaxe

``` syntax
void InterlockedMin(
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

## <a name="return-value"></a>Valeur retournée

Rien

## <a name="remarks"></a>Notes

Cette opération ne peut être effectuée que sur les ressources typées int et uint et les variables de mémoire partagée. Il existe trois utilisations possibles de cette fonction. La première est lorsque R est un type de variable de mémoire partagée. Dans ce cas, la fonction effectue un minimum atomique de la valeur dans le registre de mémoire partagée référencé par dest. Le deuxième scénario est lorsque R est un type de variable de ressource. Dans ce scénario, la fonction effectue un minimum atomique de la valeur à l’emplacement de la ressource référencé par dest. Enfin, le troisième scénario est lorsque R est un type de variable locale. Dans ce scénario, la fonction réduit à un minimum de la valeur de dest et value, stockée dans dest. La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest. Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.

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

 

 