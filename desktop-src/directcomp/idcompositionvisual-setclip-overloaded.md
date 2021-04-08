---
title: IDCompositionVisual SetClip, méthodes (Dcomp. h)
description: Définit la propriété de découpage de ce visuel sur la zone rectangulaire ou l’objet clip spécifié.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip, méthodes DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743412"
---
# <a name="idcompositionvisualsetclip-methods"></a>IDCompositionVisual :: SetClip, méthodes

Définit la propriété de découpage de ce visuel sur la zone rectangulaire ou l’objet clip spécifié. La propriété Clip restreint le rendu de la sous-arborescence visuelle qui est enracinée dans ce visuel à une région rectangulaire.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                | Description                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip (const D2D \_ rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Définit la propriété de la zone rectangulaire spécifiée.<br/> |
| [**SetClip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Affecte l’objet clip spécifié à la propriété de la séquence.<br/>        |



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

[Portion](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
