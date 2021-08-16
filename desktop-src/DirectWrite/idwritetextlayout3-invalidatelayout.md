---
title: Méthode IDWriteTextLayout3 InvalidateLayout
description: Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin. Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Écriture directe de la méthode InvalidateLayout
- Méthode InvalidateLayout Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816080"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>IDWriteTextLayout3 :: InvalidateLayout, méthode

Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin. Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                 |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





