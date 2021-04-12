---
description: Active et désactive la collecte des métriques.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Méthode ControlMetrics de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203087"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Méthode ControlMetrics de la \_ classe CIM MetricService

Active et désactive la collecte des métriques. **ControlMetrics** est utilisé pour contrôler la collection de chaque type de métrique pour un [**\_ propriété ManagedElement CIM**](cim-managedelement.md), la collection d’un type donné de métrique pour tous les éléments managés ou la collection d’une métrique spécifique pour un élément managé spécifique.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Objet* \[ dans\]
</dt> <dd>

[**\_ Propriété ManagedElement CIM**](cim-managedelement.md) qui identifie les éléments managés pour lesquels les mesures seront contrôlées.

</dd> <dt>

*Définition* \[ de dans\]
</dt> <dd>

Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les mesures seront contrôlées.

</dd> <dt>

*MetricCollectionEnabled* \[ dans\]
</dt> <dd>

Indique l’opération souhaitée à effectuer sur les mesures.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Activer** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Désactiver** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Réinitialiser** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

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

 

 




