---
description: Le \_ LoopbackMode put définit le mode de bouclage de multidiffusion.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: IMulticastControl ::p ut_LoopbackMode, méthode (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d564fbfd3e5ea0db2c168b6207823945eceb148af17d78bed25cbc59bb4e5ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140412"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>IMulticastControl ::p ut \_ LoopbackMode, méthode

\[**mettre \_ LoopbackMode** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le **\_ LoopbackMode put** définit le mode de bouclage de multidiffusion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* \[ dans\]
</dt> <dd>

[**Multidiffusion \_ \_**](multicast-loopback-mode.md) Descripteur de mode de bouclage du nouveau mode de bouclage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre de *mode* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




