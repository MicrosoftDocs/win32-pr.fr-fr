---
description: La méthode GetDisplayFormat récupère un format vidéo qui décrit le mode d’affichage actuel.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Méthode CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8841e95f4097d043e7ef01abdb067c248f43b9295a8c8466ba50f07d23bd7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074143"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>Méthode CImageDisplay. GetDisplayFormat

La `GetDisplayFormat` méthode récupère un format vidéo qui décrit le mode d’affichage actuel.

## <a name="syntax"></a>Syntaxe


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




