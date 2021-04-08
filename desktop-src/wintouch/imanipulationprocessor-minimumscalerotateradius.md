---
title: IManipulationProcessor propriété MinimumScaleRotateRadius
description: Spécifie la taille des contacts à distance sur un mouvement de mise à l’échelle ou de rotation pour déclencher la manipulation.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Touche Windows de la propriété MinimumScaleRotateRadius
- Propriété MinimumScaleRotateRadius Windows tactile, interface IManipulationProcessor
- Interface IManipulationProcessor Windows tactile, propriété MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678613"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>IManipulationProcessor :: MinimumScaleRotateRadius, propriété

Spécifie la taille des contacts à distance sur un mouvement de mise à l’échelle ou de rotation pour déclencher la manipulation.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie la distance minimale entre les contacts pour déclencher des mouvements d’échelle ou de rotation.

## <a name="error-codes"></a>Codes d’erreur

## <a name="remarks"></a>Notes

> [!Note]  
> Cette propriété est définie en centipixels (centièmes de pixel).

 

Si vous définissez cette valeur, le processeur de manipulation ignore les gestes dont le rayon est trop petit. Cela est utile si vous souhaitez empêcher un utilisateur de manipuler un objet pour qu’il soit trop petit pour un rayon. Par exemple, si vous utilisez un processeur de manipulation avec un cercle et que vous souhaitez vous assurer qu’il gère un rayon supérieur à 100 pixels, vous devez définir cette valeur sur 10000.

## <a name="examples"></a>Exemples


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




