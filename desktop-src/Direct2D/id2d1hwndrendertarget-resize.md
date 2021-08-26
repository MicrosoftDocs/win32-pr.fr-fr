---
title: ID2D1HwndRenderTarget, méthodes de redimensionnement (D2d1. h)
description: Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Redimensionner les méthodes Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 31ffcae6473924e12ca428fd48927fd1507840dce4fdbce3a18e8f82ffe9fcaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917609"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>ID2D1HwndRenderTarget :: Resize, méthodes

Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                         | Description                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Redimensionner ( \_ taille d2d1 \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Modifie la taille de la cible de rendu avec la taille de pixel spécifiée. <br/> |
| [**Redimensionner (D2D1 \_ taille \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.<br/>  |



## <a name="remarks"></a>Remarques

Après l’appel de cette méthode, le contenu de la mémoire tampon d’arrière-plan de la cible de rendu n’est pas défini, même si l’option [**d2d1 présente l’option \_ conserver le \_ \_ \_ contenu**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) a été spécifiée lors de la création de la cible de rendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
