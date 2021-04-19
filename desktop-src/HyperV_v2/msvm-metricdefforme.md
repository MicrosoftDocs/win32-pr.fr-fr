---
description: Définit l’association entre un \_ BaseMetricDefinition MSVM et un \_ propriété ManagedElement CIM pour définir des mesures pour ce dernier. La définition des métriques est donnée au contexte par propriété ManagedElement, ce qui explique pourquoi la définition dépend de l’élément.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Classe Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525049"
---
# <a name="msvm_metricdefforme-class"></a>MSVM \_ MetricDefForME, classe

Définit l’association entre un [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) et un [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) pour définir des mesures pour ce dernier. La définition des métriques est donnée au contexte par propriété ManagedElement, ce qui explique pourquoi la définition dépend de l’élément.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MetricDefForME** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MetricDefForME** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente l’élément managé qui peut avoir des métriques du type défini par **dépendant** qui lui sont appliquées. Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de la classe [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui représente la définition de la métrique à laquelle l' **antécédent** peut s’appliquer. Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**MetricCollectionEnabled**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la mesure définie par **Dependent** est collectée pour l' **antécédent**. Il s’agit de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                               | Signification                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Activé**</dt> <dt>2</dt> </dl>                                         | La mesure est collectée.<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Désactivé**</dt> <dt>3</dt> </dl>                                     | La mesure n’est pas collectée.<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Réservé**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**PartiallyEnabled**</dt> <dt>32768</dt> </dl> | La métrique est collectée pour certains périphériques, mais pas tous.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

