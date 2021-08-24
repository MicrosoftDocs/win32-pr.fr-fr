---
title: 'Texture1DArray :: Load (int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture1DArray :: Load (int, int, uint), fonction'
ms.assetid: D5877CED-BE73-4E37-B09D-4096726776EC
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
ms.openlocfilehash: 794024174f5db39fdaeb6c2cc8456764cc0751dd7363b4b367571412a8c757da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788169"
---
# <a name="texture1darrayloadintintuint-function"></a>Texture1DArray :: Load (int, int, uint), fonction

Lit les données de texture et retourne l’état de l’opération.

## <a name="syntax"></a>Syntaxe


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **int**

Coordonnées de texture.

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Type : **int**

Décalage appliqué aux coordonnées de texture avant l’échantillonnage.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Tapez :

Le type de retour correspond au type dans la déclaration pour l’objet [**Texture1DArray**](sm5-object-texture1darray.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](texture1darray-load.md)
</dt> </dl>

 

 
