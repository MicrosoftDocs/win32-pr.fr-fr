---
description: Définit une matrice de quantification.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Structure DXVA_Qmatrix_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 5d71b392d41c123eb0106d08f1a75d2a5147977b106c811e0bf0786ab2acff2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974588"
---
# <a name="dxva_qmatrix_hevc-structure"></a>DXVA \_ Qmatrix \_ HEVC, structure

Définit une matrice de quantification.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a>Membres

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

Contient les listes de mise à l’échelle pour le processus de mise à l’échelle 4x4, correspondant à ScalingList \[ 0 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus, et dont la plage est comprise entre 0 et 15 inclus.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 1 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus et que la plage est comprise entre 0 et 63 inclus.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 2 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus, et que la plage est comprise entre 0 et 63 inclus.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 3 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 1 (inclus) et que je se trouve dans la plage comprise entre 0 et 63 inclus.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contient la valeur DC de la liste de mise à l’échelle pour 16x16 size avec sizeID égal à 2 et correspondant à la mise à l’échelle \_ \_ DC \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 avec sizeID égal à 2 et matrixID dans la plage comprise entre 0 et 5 inclus, dans la spécification HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contient la valeur DC de la liste de mise à l’échelle pour une taille de 32x32 avec sizeID égal à 3, et correspondant à la mise à l’échelle \_ \_ DC \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 avec sizeID égal à 3 et matrixID dans la plage comprise entre 0 et 1 inclus, dans la spécification HEVC.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




