---
description: Représente l’état configuré des paramètres de sécurité pour.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518500"
---
# <a name="msvm_securitysettingdata-class"></a>MSVM \_ SecuritySettingData, classe

Représente l’état configuré des paramètres de sécurité pour un ordinateur virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SecuritySettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SecuritySettingData** possède les propriétés suivantes.

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour demander la protection des données pour une machine virtuelle ; Sinon, **false**. La valeur par défaut est **false**.

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour que l’État et le trafic de migration d’une machine virtuelle soient chiffrés ; Sinon, **false**. La valeur par défaut d’une machine virtuelle nouvellement créée est **false**.

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour activer un dispositif de stockage de clés (KSD) pour cet ordinateur virtuel ; Sinon, **false**. Une machine virtuelle nouvellement créée a un KSD de désactivation.

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour demander la protection d’une machine virtuelle ; Sinon, **false**. Une machine virtuelle nouvellement créée présente l’état de la protection initiale **« false »**.

</dd> <dt>

**Définit**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour activer un module de plateforme sécurisée (TPM) de plateforme sécurisée pour cet ordinateur virtuel ; Sinon, **false**. Une machine virtuelle qui vient d’être créée a un module de plateforme sécurisée désactivée.

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour ne pas offrir de sécurité basée sur la virtualisation des machines virtuelles ; Sinon, **false**. Le paramètre par défaut pour l’état de désactivation de la machine virtuelle nouvellement créée est **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

