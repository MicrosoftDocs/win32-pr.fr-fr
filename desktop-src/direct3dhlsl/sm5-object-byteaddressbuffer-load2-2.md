---
title: 'ByteAddressBuffer :: Load2 (uint, uint), fonction'
description: Obtient deux valeurs et l’état de l’opération.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
keywords:
- Load2 fonction HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031626"
---
# <a name="load2uint-uint-function"></a>Load2 (uint, uint) (fonction)

Obtient deux valeurs et l’état de l’opération.

## <a name="syntax"></a>Syntaxe

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **uint**

Adresse d’entrée en octets, qui doit être un multiple de 4.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

L’état de l’opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **uint2**

Deux valeurs.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[**ByteAddressBuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 