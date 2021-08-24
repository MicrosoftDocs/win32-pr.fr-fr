---
description: La \_ méthode obtenir LoopbackMode obtient le mode de bouclage de multidiffusion.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'IMulticastControl :: get_LoopbackMode, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013019"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>IMulticastControl :: \_ LoopbackMode, méthode

\[en **savoir \_ plus LoopbackMode** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ LoopbackMode** obtient le mode de bouclage de multidiffusion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PMODE* \[ à\]
</dt> <dd>

Pointeur vers le descripteur de [**\_ \_ mode de bouclage multicast**](multicast-loopback-mode.md) du mode de bouclage actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Signification                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *PMODE* n’est pas valide.<br/> |



 

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

 

 




