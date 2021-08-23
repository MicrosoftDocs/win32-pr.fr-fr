---
description: Affiche les métriques spécifiées.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Méthode ShowMetrics de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 052f708f07a8e1074eeaa6c8089ccd410bb63af478072545d5db92af7933fc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521469"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Méthode ShowMetrics de la \_ classe MetricService MSVM

Affiche les métriques spécifiées.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Objet* \[ dans\]
</dt> <dd>

Le paramètre subject identifie une instance de [**\_ propriété ManagedElement CIM**](cim-managedelement.md) pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques capturées pour le **\_ propriété ManagedElement CIM**.

</dd> <dt>

*Définition* \[ de dans\]
</dt> <dd>

Le paramètre de définition identifie une instance [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md). La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.

</dd> <dt>

*ManagedElements* \[ à\]
</dt> <dd>

Une fois la méthode terminée, le paramètre *ManagedElements* \[ \] peut contenir des références à [**des \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles la mesure identifiée par le paramètre de *définition* est disponible pour la collecte.

</dd> <dt>

*DefinitionList* \[ à\]
</dt> <dd>

En cas de réussite de la méthode, le paramètre *DefinitionList* peut contenir des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte pour le [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .

</dd> <dt>

*MetricNames* \[ à\]
</dt> <dd>

En cas de réussite de la méthode, chaque index de tableau du paramètre *MetricNames* doit contenir la valeur de la propriété Name pour l’instance [**du \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .

</dd> <dt>

*MetricCollectionEnabled* \[ à\]
</dt> <dd>

Le paramètre *MetricCollectionEnabled* indique si une mesure est collectée pour un élément géré.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Activer** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Désactiver** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Réservé** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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

 

 




