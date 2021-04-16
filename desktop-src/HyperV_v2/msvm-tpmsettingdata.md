---
description: Représente l’état configuré du périphérique TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527669"
---
# <a name="msvm_tpmsettingdata-class"></a>MSVM \_ TPMSettingData, classe

Représente l’état configuré du périphérique TPM.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ TPMSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ TPMSettingData** possède les propriétés suivantes.

<dl> <dt>

**DataProtected**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour définir une stratégie de protection des données d’une machine virtuelle ; Sinon, **false**. Un module de plateforme sécurisée nouvellement créé est désactivé. l’état initial de la protection des données est donc **false**.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

États activés et désactivés d’un élément. La valeur par défaut est **Disabled**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Keyprotector**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

Protecteur de clé du client du service Guardian hôte.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**
</dt> </dl>

Le dernier protecteur de clé correct connu a correctement chiffré l’état du périphérique TPM lors du dernier démarrage de la machine virtuelle.

Cette propriété est en lecture seule pour le client WMI et peut uniquement être modifiée par le périphérique TPM de la machine virtuelle.

</dd> <dt>

**Protégé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** pour définir une stratégie qui protège un ordinateur virtuel ; Sinon, **false**. Un module de plateforme sécurisée nouvellement créé est désactivé, donc l’état de la protection initiale est **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Fin de la prise en charge des clients<br/>    | Windows 10<br/>                                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

