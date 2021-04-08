---
description: Définit la luminosité de l’affichage d’un moniteur d’ordinateur.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Méthode WmiSetBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034729"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Méthode WmiSetBrightness de la classe WmiMonitorBrightnessMethods

La méthode **WmiSetBrightness** définit la luminosité d’affichage d’un moniteur d’ordinateur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Délai d'expiration* 
</dt> <dd>

Délai d’attente, en secondes.

</dd> <dt>

*Luminosité* 
</dt> <dd>

Luminosité, en pourcentage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Exemples

Pour une description détaillée de la récupération et de la définition de la luminosité du moniteur, consultez la rubrique de blog [Utiliser PowerShell pour signaler et définir la luminosité](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) de l’analyse.

L’exemple PowerShell suivant définit la luminosité de l’analyse sur 50%.


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



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

 

