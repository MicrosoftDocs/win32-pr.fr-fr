---
description: Utilisé pour définir la valeur de luminosité du capteur de lumière ambiante.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Méthode WmiSetALSBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210907"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Méthode WmiSetALSBrightness de la classe WmiMonitorBrightnessMethods

La méthode **WmiSetALSBrightness** est utilisée pour définir la valeur de luminosité du capteur de lumière ambiante. Si un remplacement de luminosité actif a été établi à l’aide de la méthode [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , ce remplacement est prioritaire par rapport à la luminosité de la als définie à l’aide de cette méthode. Pour que le remplacement de la luminosité d’un ALS activé prenne effet, la stratégie de luminosité doit être restaurée à l’aide de la méthode [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Luminosité* 
</dt> <dd>

Luminosité du ALS en pourcentage.

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

 

