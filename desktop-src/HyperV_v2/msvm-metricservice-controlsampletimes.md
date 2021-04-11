---
description: Définit les heures de l’exemple de contrôle.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Méthode ControlSampleTimes de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202764"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Méthode ControlSampleTimes de la \_ classe MetricService MSVM

Définit les heures de l’exemple de contrôle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartSampleTime* \[ dans\]
</dt> <dd>

Point dans le temps pendant lequel l’échantillonnage des mesures doit être démarré.

La valeur 99990101000000.000000 + 000 indique que l’échantillonnage doit commencer à la prochaine synchronisation à l’heure complète. L’échantillonnage est synchronisé à l’heure complète si les secondes depuis l’intervalle d’échantillonnage du modulo minuit en secondes sont égales à 0.

</dd> <dt>

*PreferredSampleInterval* \[ dans\]
</dt> <dd>

Intervalle d’échantillonnage préféré. Pour obtenir des métriques corrélées, il est recommandé de choisir l’intervalle d’échantillonnage de manière à ce que l’intervalle d’échantillonnage 3600 modulo en secondes soit égal à 0.

Il incombe à l’implémentation du service métrique CIM de déterminer si l’intervalle d’échantillonnage demandé est respecté.

Le client CIM peut vérifier si les fournisseurs de mesures respectent l’intervalle d’échantillonnage demandé en extrayant les instances BaseMetricDefinition associées et en vérifiant le contenu de la propriété « CIM \_ BaseMetricDefinition. SampleInterval ».

</dd> <dt>

*RestartGathering* \[ dans\]
</dt> <dd>

Valeur booléenne qui, lorsqu’elle est définie sur TRUE, demande que la collecte de toutes les métriques associées au service de métrique soit redémarrée avec cet appel de méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Méthode réservée** (..)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




