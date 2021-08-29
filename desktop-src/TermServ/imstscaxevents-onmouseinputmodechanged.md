---
title: Méthode IMsTscAxEvents OnMouseInputModeChanged
description: Appelé lorsque le mode d’entrée de la souris a changé.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnMouseInputModeChanged
- Méthode OnMouseInputModeChanged Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c86ce3ba30dae836077189b79553e5e39b16f53f9846f41216697d110d1dfb20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512249"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a>IMsTscAxEvents :: OnMouseInputModeChanged, méthode

Appelé lorsque le mode d’entrée de la souris a changé.

## <a name="syntax"></a>Syntaxe


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fMouseModeRelative* \[ dans\]
</dt> <dd>

Indique si la souris est en mode relatif.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le mode de saisie de la souris a changé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





