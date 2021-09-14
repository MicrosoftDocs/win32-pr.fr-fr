---
description: pour le chiffrement de lecteur ou pour créer un logiciel de sécurité de chiffrement, vous pouvez utiliser le logiciel de chiffrement Windows, Chiffrement de lecteur BitLocker, une API de chiffrement que vous pouvez utiliser à l’aide de la \_ classe de fournisseur WMI Win32 EncryptableVolume.
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b202a536f3c20126c05f072c029fe316f90ce4fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013585"
---
# <a name="win32_encryptablevolume-class"></a>\_Classe EncryptableVolume Win32

La classe de fournisseur **Win32 \_ EncryptableVolume** WMI représente une zone de stockage sur un disque dur qui peut être protégée à l’aide de chiffrement de lecteur BitLocker. Seuls les volumes NTFS peuvent être chiffrés. Il peut s’agir d’un volume qui contient un système d’exploitation ou d’un volume de données sur le disque local. Il ne peut pas s’agir d’un lecteur réseau.

Pour tirer parti des avantages de BitLocker, vous devez spécifier une méthode de protection pour la clé de chiffrement du volume, puis chiffrer entièrement le volume.

Pour protéger la clé de chiffrement du volume, ajoutez des protecteurs de clé à l’aide des méthodes suivantes :

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Chaque type de protecteur de clé fournit une expérience d’authentification différente pour le déverrouillage de l’accès aux données chiffrées. Les clés externes et les mots de passe numériques peuvent fournir une authentification pendant les scénarios de récupération. Pour les protecteurs de clé TPM, vous devrez peut-être d’abord initialiser le TPM. Pour plus d’informations, consultez la classe fournisseur WMI [**\_ TPM Win32**](win32-tpm.md) .

Utilisez la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) pour commencer le chiffrement. Vous devez ajouter les protecteurs de clé avant de commencer le chiffrement, sinon vous devez utiliser la méthode [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) pour exposer une clé en clair non protégée. Si l’ordinateur s’éteint pendant que le chiffrement est en cours, le chiffrement reprend automatiquement au redémarrage de l’ordinateur.

Vous pouvez utiliser les méthodes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) et [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) pour vérifier l’état d’un volume accessible.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ EncryptableVolume** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ EncryptableVolume** possède ces méthodes.



| Méthode                                                                                                                   | Description                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Enregistre toutes les clés externes et les informations associées nécessaires pour la récupération sur le Active Directory.<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Modifie la clé externe associée à un volume chiffré.<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Utilise la nouvelle phrase secrète pour obtenir une nouvelle clé dérivée.<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | Modifie un code confidentiel associé à un volume chiffré.<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Supprime toutes les clés externes et les informations associées enregistrées sur le volume du système d’exploitation en cours d’exécution et utilisées pour déverrouiller automatiquement les volumes de données.<br/>                                                                                                             |
| [**Crypté**](decrypt-win32-encryptablevolume.md)                                                                       | Commence le déchiffrement d’un volume entièrement chiffré ou reprend le déchiffrement d’un volume partiellement chiffré.<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Supprime un protecteur de clé donné pour le volume.<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Supprime tous les protecteurs de clé du volume.<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution, de sorte que le volume n’est pas automatiquement déverrouillé lorsqu’il est monté.<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Désactive tous les protecteurs de clé associés à ce volume.<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Permet de déverrouiller automatiquement un volume de données lorsque le volume est monté.<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Active tous les protecteurs de clé désactivés.<br/>                                                                                                                                                                                                                                       |
| [**Codage**](encrypt-win32-encryptablevolume.md)                                                                       | Commence le chiffrement d’un volume entièrement déchiffré ou reprend le chiffrement d’un volume partiellement chiffré.<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Commence le chiffrement d’un volume entièrement déchiffré après un test matériel.<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | Énumère tous les certificats sur le système qui correspondent aux critères indiqués et retourne une liste d’empreintes numériques.<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Indique l’état du chiffrement ou du déchiffrement sur le volume.<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Indique l’algorithme de chiffrement et la taille de clé utilisés sur le volume.<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Retourne le nom du fichier qui contient la clé externe.<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Retourne la clé externe à partir d’un fichier.<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Retourne des informations d’État sur un test matériel.<br/>                                                                                                                                                                                                                             |
| [**GetIdentificationField**](getidentificationfield-win32-encryptablevolume.md)                                         | Retourne la chaîne d’identificateur qui est disponible dans les métadonnées du volume.<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Retourne des informations qui permettent de récupérer les données chiffrées lorsque le lecteur est gravement endommagé.<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Récupère la clé publique et l’empreinte de certificat d’un protecteur de clé publique.<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Récupère la clé externe pour un protecteur de clé donné du type approprié.<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Récupère le nom complet utilisé pour identifier un protecteur de clé donné.<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Récupère le mot de passe numérique d’un protecteur de clé donné du type approprié.<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Récupère le profil de validation de plateforme pour un protecteur de clé donné du type approprié.<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Répertorie les protecteurs utilisés pour sécuriser la clé de chiffrement du volume.<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Indique le type d’un protecteur de clé donné.<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Indique si le contenu du volume est accessible à partir du système d’exploitation en cours d’exécution.<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Indique si le volume et sa clé de chiffrement (le cas échéant) sont sécurisés.<br/>                                                                                                                                                                                                  |
| [**GetVersion**](getversion-win32-encryptablevolume.md)                                                                 | Indique la version de métadonnées FVE du volume.<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | Indique si le volume est automatiquement déverrouillé lorsqu’il est monté.<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Indique s’il existe dans le volume du système d’exploitation en cours d’exécution toutes les clés externes et les informations associées qui peuvent être utilisées pour déverrouiller automatiquement des volumes de données.<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Indique si les protecteurs sont disponibles pour le volume.<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Indique si le mot de passe numérique répond aux exigences de format spéciales.<br/>                                                                                                                                                                                            |
| [**Verrouillage**](lock-win32-encryptablevolume.md)                                                                             | Démonte le volume et supprime la clé de chiffrement du volume de la mémoire système.<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Suspend le chiffrement ou le déchiffrement d’un volume.<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | Crée un volume BitLocker avec le type de système de fichiers spécifié du volume de détection.<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Valide l’identificateur d’objet (OID) d’utilisation améliorée de la clé (EKU) du fichier de certificat fourni.<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Valide l’identificateur d’objet (EKU) d’utilisation améliorée de la clé de l’empreinte de certificat fournie.<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Sécurise la clé de chiffrement du volume à l’aide d’une clé externe 256 bits.<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Sécurise la clé de chiffrement du volume avec un mot de passe à 48 chiffres spécialement mis en forme.<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Utilise la phrase secrète pour obtenir la clé dérivée.<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) sur l’ordinateur, le cas échéant.<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par un code confidentiel (PIN) spécifié par l’utilisateur, qui doit être fourni à l’ordinateur au démarrage.<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par un code confidentiel (PIN) spécifié par l’utilisateur et par une clé externe qui doit être fournie à l’ordinateur au démarrage.<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par une clé externe qui doit être fournie à l’ordinateur au démarrage.<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Reprend le chiffrement ou le déchiffrement d’un volume.<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Écrit la clé externe associée au protecteur de clé de volume spécifié à un emplacement de fichier spécifié.<br/>                                                                                                                                                                   |
| [**SetIdentificationField**](setidentificationfield-win32-encryptablevolume.md)                                         | Définit la chaîne d’identificateur spécifiée dans les métadonnées du volume.<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Utilise le fichier de certificat fourni pour obtenir la clé dérivée et déverrouiller le volume chiffré.<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Utilise l’empreinte de certificat fournie pour obtenir la clé dérivée et déverrouiller le volume chiffré.<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Utilise une clé externe fournie pour accéder au contenu d’un volume de données.<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Utilise un mot de passe numérique fourni pour accéder au contenu d’un volume de données.<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Utilise la phrase secrète pour obtenir la clé dérivée. Une fois la clé dérivée calculée, la clé dérivée est utilisée pour déverrouiller la clé principale du volume chiffré.<br/>                                                                                                                   |
| [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md)                                                           | met à niveau un volume du format Windows Vista au format Windows 7.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ EncryptableVolume** a ces propriétés.

<dl> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identificateur unique du volume sur ce système. À utiliser pour associer un volume à d’autres classes de fournisseur WMI, par exemple, le **\_ volume Win32**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Lettre de lecteur du volume. Cet identificateur peut être utilisé pour associer un volume à d’autres classes de fournisseur WMI, par exemple le [**\_ volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)).

Pour les volumes sans lettres de lecteur, cette valeur est **null**.

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur persistant pour le volume sur ce système. Cet identificateur est exclusif à **Win32 \_ EncryptableVolume**.

Cet identificateur est une chaîne vide si le volume est un volume NTFS standard entièrement déchiffré ; dans le cas contraire, elle a une valeur unique.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État du volume, que BitLocker protège ou non le volume. Cette valeur est stockée lorsque la classe est instanciée. L’état de protection peut modifier l’état entre l’instanciation et le moment où vous vérifiez la valeur. Pour vérifier la valeur de la propriété **ProtectionStatus** en temps réel, utilisez la méthode [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .



| Valeur                                                                        | Signification                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | PROTECTION DÉSACTIVÉE<br/> Le volume n’est pas chiffré, partiellement chiffré ou la clé de chiffrement du volume est disponible en clair sur le disque dur. <br/> |
| <dl> <dt>1</dt> </dl> | PROTECTION ACTIVÉE<br/> Le volume est entièrement chiffré et la clé de chiffrement du volume n’est pas disponible en clair sur le disque dur. <br/>                          |
| <dl> <dt>2</dt> </dl> | PROTECTION INCONNUE<br/> Impossible de déterminer l’état de la protection du volume. L’une des causes possibles est que le volume est dans un état verrouillé.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Considérations relatives à la sécurité

La classe de fournisseur **Win32 \_ EncryptableVolume** WMI repose sur la sécurité de l’espace de noms WMI et sur le sous-système chiffrement de lecteur BitLocker pour le contrôle d’accès.

Pour utiliser les méthodes **Win32 \_ EncryptableVolume** , les conditions suivantes doivent être remplies :

-   Vous devez disposer de privilèges d’administrateur.
-   Le chiffrement de la connexion doit être en mesure de se connecter au fournisseur.

    Pour plus d’informations sur la création d’une connexion chiffrée, consultez [demande d’une connexion chiffrée à un espace de noms](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md).

Pour activer les connexions à distance, le trafic WMI distant doit être autorisé. Pour plus d’informations sur l’activation du trafic WMI, consultez [connexion à WMI à distance à partir de Vista](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md).

Le paramètre de sécurité espace de noms par défaut comprend une entrée pour permettre la modification par défaut. Pour plus d’informations sur l’audit de l’espace de noms WMI, consultez [accès aux espaces de noms WMI](../wmisdk/access-to-wmi-namespaces.md).

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



 

 
