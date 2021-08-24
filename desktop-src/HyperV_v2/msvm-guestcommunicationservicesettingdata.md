---
description: Représente les paramètres du service de communication invité.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Classe Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67026a1dd7e605effb923305c45d329e7a2a502fe0324f00d2ddcf346c899778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148048"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a>MSVM \_ GuestCommunicationServiceSettingData, classe

Représente les paramètres du service de communication invité.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestCommunicationServiceSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestCommunicationServiceSettingData** possède les propriétés suivantes.

<dl> <dt>

**EnabledStatePolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

EnabledStatePolicy est une énumération entière qui indique l’état activé, désactivé ou par défaut **du \_ GuestCommunicationServiceSettingData MSVM**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)


</dt> <dd>

Le service de communication est défini sur l’état activé.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)


</dt> <dd>

Le service de communication est défini sur l’état désactivé.

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)


</dt> <dd>

L’état du service de communication dépend de **DefaultEnabledStatePolicy** dans **MSVM \_ GuestCommunicationServiceSettingData**.

</dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID du service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




