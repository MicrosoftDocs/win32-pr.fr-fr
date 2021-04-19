---
description: Vérifie si la réplication peut être activée à partir du système hôte actuel vers le système de récupération spécifié.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Méthode TestReplicationConnection de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544618"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Méthode TestReplicationConnection de la \_ classe ReplicationService MSVM

Vérifie si la réplication peut être activée à partir du système hôte actuel vers le système de récupération spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RecoveryConnectionPoint* \[ dans\]
</dt> <dd>

Nom du point de connexion. Pour un cluster de récupération, il s’agit du nom de l’extrémité de service Broker. Pour un serveur de récupération autonome, il s’agit du nom du système hôte.

</dd> <dt>

*RecoveryServerPortNumber* \[ dans\]
</dt> <dd>

Numéro de port du point de connexion de récupération.

</dd> <dt>

*AuthenticationType* \[ dans\]
</dt> <dd>

Schéma d’authentification de récupération. Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Authentification intégrée** (1)


</dt> <dd>

Authentification Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Authentification basée sur les certificats** (2)


</dt> <dd>

Authentification basée sur les certificats.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ dans\]
</dt> <dd>

Empreinte numérique du certificat à utiliser lorsque le paramètre *AuthenticationType* est l’authentification basée sur les certificats.

</dd> <dt>

*BypassProxyServer* \[ dans\]
</dt> <dd>

Contournez le serveur proxy lors de la connexion au serveur de réplication.

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

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> <dt>

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

