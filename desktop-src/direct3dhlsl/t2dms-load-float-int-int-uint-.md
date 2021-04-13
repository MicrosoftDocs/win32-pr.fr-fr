---
title: 'Texture2DMS :: Load (int, int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture2DMS :: Load (int, int, int, uint), fonction'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321805"
---
# <a name="texture2dmsloadintintintuint-function"></a>Texture2DMS :: Load (int, int, int, uint), fonction

Lit les données de texture et retourne l’état de l’opération.

## <a name="syntax"></a>Syntaxe


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **Int2**

Coordonnées de texture.

</dd> <dt>

*sampleindex* \[ dans\]
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Exemple d’index.

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Type : **Int2**

Décalage appliqué aux coordonnées de texture avant le chargement.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

L’état de l’opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Tapez :

Le type de retour correspond au type dans la déclaration pour l’objet [**Texture2DMS**](sm5-object-texture2dms.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
