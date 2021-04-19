---
description: Affiche les métriques par classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Méthode ShowMetricsByClass de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544841"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Méthode ShowMetricsByClass de la \_ classe MetricService MSVM

Affiche les métriques par classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Objet* \[ dans\]
</dt> <dd>

Identifie une classe CIM pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques qui peuvent être capturées pour toutes les instances de la classe.

</dd> <dt>

*Définition* \[ de dans\]
</dt> <dd>

Identifie une instance de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md). La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.

</dd> <dt>

*DefinitionList* \[ à\]
</dt> <dd>

Une fois la méthode terminée, peut contenir des références à des instances [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte du [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .

</dd> <dt>

*MetricNames* \[ à\]
</dt> <dd>

Une fois la méthode terminée, chaque index de tableau contient la valeur de la propriété **Name** pour l’instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .

</dd> <dt>

*MetricCollectionEnabled* \[ à\]
</dt> <dd>

Indique si une mesure est collectée pour toutes les instances d’une classe d’éléments managés.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (3)


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

La méthode retourne l'une des valeurs suivantes :

<dl> <dt>

**Opération réussie** ()
</dt> <dt>

**Non pris en charge** ()
</dt> <dt>

**Échec** ()
</dt> <dt>

**Méthode réservée** ()
</dt> <dt>

**Spécifique au fournisseur** ()
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

 

 




