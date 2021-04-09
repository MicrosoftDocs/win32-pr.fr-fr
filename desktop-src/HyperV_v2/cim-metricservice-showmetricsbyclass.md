---
description: 'Signale les éléments suivants : les métriques pouvant être collectées pour toutes les instances d’une classe CIM, les classes CIM pour lesquelles une mesure définie par une instance de CIM \_ BaseMetricDefinition est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Méthode ShowMetricsByClass de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865541"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Méthode ShowMetricsByClass de la \_ classe CIM MetricService

Signale les éléments suivants : les métriques pouvant être collectées pour toutes les instances d’une classe CIM, les classes CIM pour lesquelles une mesure définie par une instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.

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

En cas de réussite, peut contenir des références à des instances d’objets [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte pour le [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .

</dd> <dt>

*MetricNames* \[ à\]
</dt> <dd>

En cas de réussite, chaque index de tableau doit contenir la valeur de la propriété **Name** pour l’instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .

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

 

 




