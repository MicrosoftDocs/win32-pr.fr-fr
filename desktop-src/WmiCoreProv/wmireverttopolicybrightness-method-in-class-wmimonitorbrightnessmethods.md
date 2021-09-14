---
description: La méthode WmiRevertToPolicyBrightness est utilisée pour rétablir la luminosité du paramètre de stratégie. Cette méthode n’a aucun effet sur les paramètres de luminosité du ALS.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Méthode WmiRevertToPolicyBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855609"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Méthode WmiRevertToPolicyBrightness de la classe WmiMonitorBrightnessMethods

La méthode **WmiRevertToPolicyBrightness** est utilisée pour rétablir la luminosité du paramètre de stratégie. Cette méthode n’a aucun effet sur les paramètres de luminosité du ALS.

## <a name="syntax"></a>Syntaxe


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Spécifications



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

 

