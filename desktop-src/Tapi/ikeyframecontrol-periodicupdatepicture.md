---
description: La méthode PeriodicUpdatePicture est appelée par une application pour configurer un minuteur dans le flux qui demandera régulièrement des mises à jour d’images. Les mises à jour d’image entraînent une utilisation élevée de la bande passante. cette méthode est donc normalement utilisée à la place de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: IKeyFrameControl ::P méthode eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539192"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>IKeyFrameControl ::P méthode eriodicUpdatePicture

\[**PeriodicUpdatePicture** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **PeriodicUpdatePicture** est appelée par une application pour configurer un minuteur dans le flux qui demandera régulièrement des mises à jour d’images. Les mises à jour d’image entraînent une utilisation élevée de la bande passante. cette méthode est donc normalement utilisée à la place de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).

Si la méthode est appelée lorsque le flux est actif, le minuteur démarre immédiatement. Si le flux n’est pas actif, le minuteur est démarré lorsque le flux passe à l’état actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnable* \[ dans\]
</dt> <dd>

**True** active la minuterie. **False** le désactive.

</dd> <dt>

*dwInterval* \[ dans\]
</dt> <dd>

Intervalle, en secondes, de la minuterie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | La méthode a réussi.<br/>              |
| <dl> <dt>**E \_ échec**</dt> </dl> | A échoué pour des raisons inattendues.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

 




