---
description: Représente les paramètres pour le service synthétique 3D présent sur un système hôte unique.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Classe Msvm_Synthetic3DServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114958"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a>MSVM \_ Synthetic3DServiceSettingData, classe

Représente les paramètres pour le service synthétique 3D présent sur un système hôte unique. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la méthode [**MSVM \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) pour modifier l’une de ces propriétés.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ Synthetic3DServiceSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ Synthetic3DServiceSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**GPUOvercommitEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contrôle si l’attribution de l’ordinateur virtuel prend en compte les limitations de mémoire du GPU.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

