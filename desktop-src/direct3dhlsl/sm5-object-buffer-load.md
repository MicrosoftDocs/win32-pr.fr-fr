---
title: 'Fonction buffer :: Load (int, uint)'
description: 'Lit les données de mémoire tampon et retourne l’état de l’opération. | Fonction buffer :: Load (int, uint)'
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232211"
---
# <a name="bufferloadint-uint-function"></a>Fonction buffer :: Load (int, uint)

Lit les données de mémoire tampon et retourne l’état de l’opération.

## <a name="syntax"></a>Syntaxe

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **int**

Emplacement de la mémoire tampon.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Tapez :

Le type de retour correspond au type dans la déclaration pour l’objet de [**mémoire tampon**](sm5-object-buffer.md) .

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="examples"></a>Exemples

Cet exemple montre comment utiliser **Load**:

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](buffer-load.md)
</dt> </dl>

 

 
