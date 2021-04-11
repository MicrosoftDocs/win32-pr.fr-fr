---
title: Méthodes IDCompositionVisual SetTransform (Dcomp. h)
description: Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 2D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 3 par 2 ou un objet de transformation.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317442"
---
# <a name="idcompositionvisualsettransform-methods"></a>IDCompositionVisual :: SetTransform, méthodes

Définit la propriété de transformation de cet visuel. La propriété transformer spécifie une transformation 2D utilisée pour modifier le système de coordonnées de cet visuel. La propriété peut spécifier une matrice de transformation 3 par 2 ou un objet de transformation.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                    | Description                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform ( \_ matrice D2D \_ matrice \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Définit la propriété de transformation sur la matrice de transformation spécifiée.<br/>      |
| [**SetTransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Définit la propriété de transformation sur l’objet de transformation spécifié.<br/> |



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
