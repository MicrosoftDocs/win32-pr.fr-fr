---
description: Représente les paramètres pour le service de métrique. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la méthode ModifyServiceSettings pour modifier l’une de ces propriétés.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Classe Msvm_MetricServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff0c8b9e4212624f4643efb7f7ef67ea4bc72f9488caa1b43d6260c9949011ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521319"
---
# <a name="msvm_metricservicesettingdata-class"></a>MSVM \_ MetricServiceSettingData, classe

Représente les paramètres pour le service de métrique. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) pour modifier l’une de ces propriétés.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MetricServiceSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MetricServiceSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. cette propriété est héritée de [**CIM \_ propriété managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Hyper-V Metric Service Paramètres ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . cette propriété est héritée de [**CIM \_ propriété managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définit le Service métrique Hyper-V Paramètres ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. cette propriété est héritée de [**CIM \_ propriété managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Hyper-V Metric Service Paramètres ».

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**MetricsFlushInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Définit l’intervalle auquel les mesures doivent être vidées sur le disque.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

