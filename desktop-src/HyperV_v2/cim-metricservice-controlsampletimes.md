---
description: Autorise la spécification de la collecte des métriques dans le temps à démarrer et à spécifier l’intervalle d’échantillonnage préféré pour la collecte de données périodique.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Méthode ControlSampleTimes de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527506"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>Méthode ControlSampleTimes de la \_ classe CIM MetricService

Autorise la spécification de la collecte des métriques dans le temps à démarrer et à spécifier l’intervalle d’échantillonnage préféré pour la collecte de données périodique.

Chaque fois que l’échantillonnage pour des métriques supplémentaires est démarré, les paramètres spécifiés par cette méthode peuvent être utilisés.

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

Le client CIM peut vérifier si les fournisseurs de mesures respectent l’intervalle d’échantillonnage demandé en extrayant les instances BaseMetricDefinition associées et en vérifiant le contenu du [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).**Propriété SampleInterval** .

</dd> <dt>

*RestartGathering* \[ dans\]
</dt> <dd>

**True** pour demander que la collecte de toutes les métriques associées au service de métrique soit redémarrée avec cet appel de méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

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

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




