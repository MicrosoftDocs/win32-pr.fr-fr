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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006705"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Méthode CPersistStream. GetSoftwareVersion

Récupère la version du logiciel pour ce flux.

## <a name="syntax"></a>Syntaxe


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une **valeur DWORD** contenant le numéro de version. Chaque fois que le format du flux est modifié, cette fonction doit être modifiée pour retourner un nombre plus élevé qu’avant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




