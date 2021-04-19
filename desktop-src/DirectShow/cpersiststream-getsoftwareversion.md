---
description: Récupère la version du logiciel pour ce flux.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Méthode CPersistStream. GetSoftwareVersion (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535248"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Méthode CPersistStream. GetSoftwareVersion

Récupère la version du logiciel pour ce flux.

## <a name="syntax"></a>Syntaxe


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une **valeur DWORD** contenant le numéro de version. Chaque fois que le format du flux est modifié, cette fonction doit être modifiée pour retourner un nombre plus élevé qu’avant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PStream. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




