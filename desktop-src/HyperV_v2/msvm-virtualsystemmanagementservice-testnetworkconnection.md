---
description: teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Méthode TestNetworkConnection de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388378"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode TestNetworkConnection de la \_ classe VirtualSystemManagementService MSVM

teste la connectivité réseau d’une machine virtuelle dans un environnement de virtualisation de réseau Windows.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TargetNetworkAdapter* \[ dans\]
</dt> <dd>

Référence à un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) décrivant la carte réseau cible.

</dd> <dt>

*IsSender* \[ dans\]
</dt> <dd>

Indique si cette méthode est appelée au niveau de l’expéditeur ou du récepteur.

</dd> <dt>

*SenderIP* \[ dans\]
</dt> <dd>

Adresse IP de l’expéditeur.

</dd> <dt>

*ReceiverIP* \[ dans\]
</dt> <dd>

Adresse MAC de l’expéditeur.

</dd> <dt>

*ReceiverMac* \[ dans\]
</dt> <dd>

Adresse MAC de l’expéditeur.

</dd> <dt>

*IsolationId* \[ dans\]
</dt> <dd>

ID d’isolation.

</dd> <dt>

 N \[ dans\]
</dt> <dd>

ID d’isolation.

</dd> <dt>

*RoundtripTime* \[ à\]
</dt> <dd>

Durée de l’aller-retour.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

