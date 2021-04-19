---
description: Contrôle les métriques par classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Méthode ControlMetricsByClass de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524688"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Méthode ControlMetricsByClass de la \_ classe MetricService MSVM

Contrôle les métriques par classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Objet* \[ dans\]
</dt> <dd>

Identifie la classe CIM pour laquelle les mesures seront contrôlées.

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

 

 




