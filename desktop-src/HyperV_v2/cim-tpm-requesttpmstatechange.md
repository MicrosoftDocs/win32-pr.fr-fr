---
description: Demande que l’état du module de plateforme sécurisée soit remplacé par la valeur spécifiée dans le paramètre RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Méthode RequestTPMStateChange de la classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 94af1d619ffa686b2fb4546987c6b825e4c658a5ae045d84fe5c6181716e95e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646447"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Méthode RequestTPMStateChange de la \_ classe TPM CIM

Demande que l’état du module de plateforme sécurisée soit remplacé par la valeur spécifiée dans le paramètre *RequestedTPMState* . Si l’appel de la méthode se termine correctement, la propriété **TPMState** sera égale au paramètre **RequestedTPMState** . L’appel de la méthode **RequestTPMStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedTPMState* \[ dans\]
</dt> <dd>

États du module de plateforme sécurisée demandé.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 activé-propriétaire actif** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 désactivé-actif-propriétaire** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 activé-inactif-détenu** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 désactivé-inactif-détenu** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 activé-actif-sans propriétaire** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 désactivé-actif-non détenu** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 activé-inactif-sans propriétaire** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 désactivé-inactif-sans propriétaire** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ dans\]
</dt> <dd>

Jeton d’autorisation qui peut être nécessaire pour que l’action prenne effet. Le paramètre *AuthorizationToken* peut être nécessaire pour établir la présence physique, ou pour transmettre le origine, le mot de passe d’autorisation du propriétaire défini par le TCG. Dans le cas de origine, le \_ SHAREDCREDENTIAL CIM avec la valeur non null du CIM \_ SharedCredential. secret peut être requis. La \_ propriété CIM SharedCredential. algorithme peut également être spécifiée en fonction de la propriété CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Peut contenir une référence au [**\_ ConcreteJob CIM**](cim-concretejob.md) créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le *TimeoutPeriod*. La valeur 0 ou un paramètre null indique que le client n’a aucune exigence de temps pour la transition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Erreur inconnue ou non spécifiée** (2)
</dt> <dt>

**Impossible de se terminer dans le délai imparti** (3)
</dt> <dt>

**Échec** (4)
</dt> <dt>

**Paramètre non valide** (5)
</dt> <dt>

**En cours d’utilisation** (6)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Transition d’État non valide** (4097)
</dt> <dt>

**Utilisation du paramètre timeout non prise en charge** (4098)
</dt> <dt>

**Occupé** (4099)
</dt> <dt>

**Méthode réservée** (4100.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

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

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




