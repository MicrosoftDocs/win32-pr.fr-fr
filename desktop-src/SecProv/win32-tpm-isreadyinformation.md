---
description: Indique si le module de plateforme sécurisée est prêt et fournit des informations supplémentaires sur l’état du module de plateforme sécurisée.
ms.assetid: 1E348D77-979C-42FC-824D-7C57F7BAABE5
title: 'Win32_Tpm :: IsReadyInformation, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReadyInformation
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 23f3b2f38ea12bac19230f1871d30c84098eb1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952698"
---
# <a name="win32_tpmisreadyinformation-method"></a>Win32 \_ TPM :: IsReadyInformation, méthode

Indique si le module de plateforme sécurisée est prêt et fournit des informations supplémentaires sur l’état du module de plateforme sécurisée. Le paramètre information renvoie un masque de données qui indique ce qui est nécessaire pour approvisionner entièrement le module de plateforme sécurisée.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsReady* \[ à\]
</dt> <dd>

Affectez la valeur **true** si le module de plateforme sécurisée et le système sont entièrement approvisionnés pour une utilisation TPM.

</dd> <dt>

*Informations* \[ à\]
</dt> <dd>

Retourne un masque de données avec autant d’informations que nécessaire pour approvisionner entièrement le module de plateforme sécurisée.

Le paramètre d' *information* peut comporter les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**Informations \_ ARRÊT**</dt> <dt>0x00000002</dt> </dl>                                                 | Le redémarrage de la plateforme est nécessaire (arrêt).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**Informations \_ REDÉMARRER**</dt> <dt>0x00000004</dt> </dl>                                                       | Le redémarrage de la plateforme est nécessaire (redémarrage).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**Informations \_ \_Forcer l' \_ effacement du module de plateforme sécurisée**</dt> <dt></dt> </dl>                          | Le module de plateforme sécurisée est déjà détenu. Soit le module de plateforme sécurisée doit être effacé, soit la valeur d’autorisation du propriétaire du module de plateforme sécurisée doit être importée.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**Informations \_ \_Présence physique**</dt> <dt>0x00000010</dt> </dl>                     | Une présence physique est nécessaire pour approvisionner le module de plateforme sécurisée.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**Informations \_ \_Activer le module de plateforme sécurisée**</dt> <dt>0x00000020</dt> </dl>                                    | Le module de plateforme sécurisée est désactivé ou désactivé.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**Informations \_ 0x00000040 TPM \_ Take \_ Ownership**</dt> <dt></dt> </dl>                 | La propriété du module de plateforme sécurisée a été prise.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**Informations \_ \_ \_ Créer**</dt> un <dt>0x00000080</dt> EK de TPM </dl>                                | Une clé de type EK (EK) existe dans le module de plateforme sécurisée. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**Informations \_ Module de plateforme sécurisée \_ origine**</dt> <dt>0x00000100</dt> </dl>                                 | L’autorisation du propriétaire du module de plateforme sécurisée n’est pas correctement stockée dans le registre.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Informations \_ 0x00000200 \_ d' \_ authentification TPM SRK**</dt> <dt></dt> </dl>                                  | La valeur d’autorisation de la clé de racine de stockage (SRK) n’est pas égale à zéro.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Informations \_ Désactivation désactive le \_ \_ propriétaire \_ du module de plateforme sécurisée**</dt> <dt>0x00000400</dt> </dl> | Si le système d’exploitation est configuré pour désactiver l’effacement du module de plateforme sécurisée avec la valeur d’autorisation du propriétaire du module de plateforme sécurisée et que le module de plateforme sécurisée n’a pas encore été configuré pour empêcher l’effacement du TPM avec la valeur d’autorisation du propriétaire du module<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Informations \_ Module de plateforme sécurisée \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | Les informations de Registre du système d’exploitation relatives à la clé racine de stockage du module de plateforme sécurisée ne correspondent pas à la clé racine de stockage GPC.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Informations \_ \_ \_ SRKPUB de lecture TPM**</dt> <dt>0x00001000</dt> </dl>                          | L’indicateur permanent TPM pour permettre la lecture de la valeur publique de la clé racine de stockage n’est pas défini.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Informations \_ 0x00002000 \_ du \_ compteur de démarrage TPM**</dt> <dt></dt> </dl>                       | Le compteur monotone incrémenté au cours du démarrage n’a pas été créé.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Informations \_ 0x00004000 \_ de \_ sauvegarde ad TPM**</dt> <dt></dt> </dl>                                | L’autorisation du propriétaire du module de plateforme sécurisée n’a pas été sauvegardée dans Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Informations \_ \_Phase de \_ sauvegarde \_ \_ ad TPM**</dt> <dt>0x00008000</dt> </dl>      | La première partie du stockage des informations d’autorisation du propriétaire du module de plateforme sécurisée dans Active Directory est en cours.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Informations \_ \_Sauvegarde ad TPM- \_ \_ phase \_ II**</dt> <dt>0x00010000</dt> </dl>   | La deuxième partie du stockage des informations d’autorisation du propriétaire du module de plateforme sécurisée dans Active Directory est en cours.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Informations \_ \_Configuration héritée**</dt> <dt>0x00020000</dt> </dl>            | Windows stratégie de groupe est configuré pour ne pas stocker l’autorisation du propriétaire du module de plateforme sécurisée afin que le module de plateforme sécurisée ne puisse pas être entièrement prêt.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Informations \_ 0x00040000 \_ certificat EK**</dt> <dt></dt> </dl>                              | Le certificat EK n’a pas été lu à partir de la RAM NV TPM et stocké dans le registre. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Informations \_ 0x00080000 \_ du \_ Journal des événements TCG**</dt> <dt></dt> </dl>                                | Le journal des événements TCG est vide ou ne peut pas être lu. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Informations \_ 0x00100000 non \_ réduit**</dt> <dt></dt> </dl>                                       | Le module de plateforme sécurisée n’est pas détenu.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Informations \_ \_Erreur générique**</dt> <dt>0x00200000</dt> </dl>                                 | Une erreur s’est produite, mais elle n’est pas spécifique à une tâche particulière.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Informations \_ \_ \_ Compteur de verrous d’appareil**</dt> <dt>0x00400000</dt> </dl>              | Le compteur de verrouillage de l’appareil n’a pas été créé.<br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <dt>**Informations \_ DEVICEID**</dt> <dt> 0x00800000</dt> </dl>                                                | L’identificateur de l’appareil n’a pas été créé.<br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <dt>**Informations \_ \_Vulnérabilité d’attestation**</dt> <dt> 0x01000000</dt> </dl>                                                | Le module de plateforme sécurisée présente une vulnérabilité liée à l’attestation d’intégrité.<br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | \\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
