---
description: Tente d’approvisionner le module de plateforme sécurisée dans un État entièrement prêt et prend la propriété du module de plateforme sécurisée s’il n’est pas déjà détenu.
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm ::P méthode rovision
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5153672d91c88597676f65b53a93de6ffac9f4989dd9e231c87a3b7947b1d657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890807"
---
# <a name="win32_tpmprovision-method"></a>\_TPM Win32 ::P méthode rovision

Tente d’approvisionner le module de plateforme sécurisée dans un État entièrement prêt et prend la propriété du module de plateforme sécurisée s’il n’est pas déjà détenu. Cette méthode est coûteuse à s’exécuter, car elle effectue de nombreuses vérifications. Il s’agit d’applications recommandées qui utilisent cette méthode uniquement lorsque cela est nécessaire.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ForceClear \_ Autorisé* \[ dans\]
</dt> <dd>

Si la valeur est **true** , la méthode peut demander des opérations de présence physique pour effacer le module de plateforme sécurisée. Si la valeur est **false**, la méthode ne demande pas une opération de présence physique pour effacer le module de plateforme sécurisée.

</dd> <dt>

*PhysicalPresencePrompts \_ Autorisé* \[ dans\]
</dt> <dd>

Si la valeur est **true** , la méthode peut demander des opérations de présence physique qui requièrent l’implication de l’utilisateur pendant le processus de démarrage pour confirmer la modification de l’état du module de plateforme sécurisée.

</dd> <dt>

*Informations* \[ à\]
</dt> <dd>

Retourne un masque de données avec autant d’informations que nécessaire pour approvisionner entièrement le module de plateforme sécurisée. Les valeurs de masque comme \_ redémarrage des informations indiquent que l’appel de méthode doit lancer un redémarrage pour déplacer le processus de déploiement.

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
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Informations \_ 0x000000200 \_ d' \_ authentification TPM SRK**</dt> <dt></dt> </dl>                                  | la valeur d’autorisation de la clé racine de l’Stockage n’est pas égale à zéro.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Informations \_ Désactivation désactive le \_ \_ propriétaire \_ du module de plateforme sécurisée**</dt> <dt>0x00000400</dt> </dl> | Si le système d’exploitation est configuré pour désactiver l’effacement du module de plateforme sécurisée avec la valeur d’autorisation du propriétaire du module de plateforme sécurisée et que le module de plateforme sécurisée n’a pas encore été configuré pour empêcher l’effacement du TPM avec la valeur d’autorisation du propriétaire du module<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Informations \_ Module de plateforme sécurisée \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | les informations de registre du système d’exploitation relatives à la clé racine du module de plateforme sécurisée Stockage ne correspondent pas à la clé racine du module de plateforme sécurisée Stockage.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Informations \_ \_ \_ SRKPUB de lecture TPM**</dt> <dt>0x00001000</dt> </dl>                          | l’indicateur permanent TPM pour permettre la lecture de la valeur publique de la clé racine Stockage n’est pas défini.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Informations \_ 0x00002000 \_ du \_ compteur de démarrage TPM**</dt> <dt></dt> </dl>                       | Le compteur monotone incrémenté au cours du démarrage n’a pas été créé.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Informations \_ 0x00004000 \_ de \_ sauvegarde ad TPM**</dt> <dt></dt> </dl>                                | L’autorisation du propriétaire du module de plateforme sécurisée n’a pas été sauvegardée dans Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Informations \_ \_Phase de \_ sauvegarde \_ \_ ad TPM**</dt> <dt>0x00008000</dt> </dl>      | La première partie du stockage des informations d’autorisation du propriétaire du module de plateforme sécurisée dans Active Directory est en cours.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Informations \_ \_Sauvegarde ad TPM- \_ \_ phase \_ II**</dt> <dt>0x00010000</dt> </dl>   | La deuxième partie du stockage des informations d’autorisation du propriétaire du module de plateforme sécurisée dans Active Directory est en cours.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Informations \_ \_Configuration héritée**</dt> <dt>0x00020000</dt> </dl>            | Windows Stratégie de groupe est configurée pour ne pas stocker l’autorisation du propriétaire du module de plateforme sécurisée, de sorte que le TPM ne peut pas être entièrement prêt.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Informations \_ 0x00040000 \_ certificat EK**</dt> <dt></dt> </dl>                              | Le certificat EK n’a pas été lu à partir de la RAM NV TPM et stocké dans le registre. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Informations \_ 0x00080000 \_ du \_ Journal des événements TCG**</dt> <dt></dt> </dl>                                | Le journal des événements TCG est vide ou ne peut pas être lu. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Informations \_ 0x00100000 non \_ réduit**</dt> <dt></dt> </dl>                                       | Le module de plateforme sécurisée n’est pas détenu.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Informations \_ \_Erreur générique**</dt> <dt>0x00200000</dt> </dl>                                 | Une erreur s’est produite, mais elle n’est pas spécifique à une tâche particulière.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Informations \_ \_ \_ Compteur de verrous d’appareil**</dt> <dt>0x00400000</dt> </dl>              | Le compteur de verrouillage de l’appareil n’a pas été créé.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | \\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
