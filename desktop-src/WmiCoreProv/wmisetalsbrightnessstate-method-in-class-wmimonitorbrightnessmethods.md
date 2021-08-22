---
description: Utilisé pour contrôler l’état de luminosité du capteur de lumière ambiante.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Méthode WmiSetALSBrightnessState de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051117"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Méthode WmiSetALSBrightnessState de la classe WmiMonitorBrightnessMethods

La méthode **WmiSetALSBrightnessState** est utilisée pour contrôler l’état de luminosité du capteur de lumière ambiante. Si un remplacement de luminosité actif a été établi à l’aide de la méthode [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , ce remplacement est prioritaire par rapport à la luminosité de la als définie à l’aide de cette méthode. Pour que le remplacement de la luminosité d’un ALS activé prenne effet, la stratégie de luminosité doit être restaurée à l’aide de la méthode [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*State* 
</dt> <dd>

État de luminosité du ALS. La valeur False désactive le remplacement de luminosité ALS et la valeur true l’active.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

