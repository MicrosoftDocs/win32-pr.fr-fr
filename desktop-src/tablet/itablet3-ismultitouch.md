---
description: Détermine si un périphérique d’entrée prend en charge l’interaction tactile multipoint.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3 :: IsMultiTouch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: bbdd18d27c8b9f5f4b7567e6aa22fd0c74f5e2c2dc74d80e1f46aca4195b93ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717298"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3 :: IsMultiTouch, méthode

Détermine si un périphérique d’entrée prend en charge l’interaction tactile multipoint.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIsMultiTouch* \[ à\]
</dt> <dd>

Indique si l’appareil est en interaction tactile.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite, sinon retourne un code d’erreur tel que **E \_ Fail**.

## <a name="remarks"></a>Remarques

Après avoir déterminé à l’aide de [**IRealTimeStylus3 :: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) ou **ITablet3 :: IsMultiTouch** que l’interaction tactile est disponible, une application peut choisir d’accepter les messages d’entrée tactiles. Des informations supplémentaires sur le filtrage des méthodes tactiles sont disponibles dans la section de propriété **IRealTimeStylus3 :: MultiTouchEnabled** .

## <a name="examples"></a>Exemples


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




