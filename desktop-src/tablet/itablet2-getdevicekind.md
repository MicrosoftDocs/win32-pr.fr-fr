---
description: Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2 :: GetDeviceKind, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450526"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2 :: GetDeviceKind, méthode

Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pKind* \[ à\]
</dt> <dd>

Valeur d’énumération qui indique le type de tablette, par exemple la souris, le stylet ou le toucher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Remarques

cette interface et cette méthode ont été introduites dans Windows Vista.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITablet2**](itablet2.md)
</dt> <dt>

[**\_Énumération de type d’appareil tablette \_**](tablet-device-kind.md)
</dt> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




