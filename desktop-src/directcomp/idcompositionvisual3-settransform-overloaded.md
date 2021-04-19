---
title: Méthodes IDCompositionVisual3 SetTransform (Dcomp. h)
description: Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 3D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 4-par-4 ou un objet de transformation.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Méthodes SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510967"
---
# <a name="idcompositionvisual3settransform-methods"></a>IDCompositionVisual3 :: SetTransform, méthodes

Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 3D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 4-par-4 ou un objet de transformation.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                  | Description                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform ( \_ matrice D2D \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Définit la propriété de transformation sur la matrice de transformation spécifiée.<br/>      |
| [**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Définit la propriété de transformation sur l’objet de transformation spécifié.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Dcomp. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Dcomp. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
