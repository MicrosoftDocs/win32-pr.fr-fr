---
description: Sauvegarde les données de récupération dans Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Méthode BackupRecoveryInformationToActiveDirectory de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545152"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Méthode BackupRecoveryInformationToActiveDirectory de la \_ classe Win32 EncryptableVolume

La méthode **BackupRecoveryInformationToActiveDirectory** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sauvegarde les données de récupération dans Active Directory. Cette méthode nécessite la présence d’un protecteur de mot de passe numérique sur le volume. Stratégie de groupe doit également être configuré pour permettre la sauvegarde des informations de récupération sur Active Directory.

## <a name="syntax"></a>Syntaxe


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré. Ce protecteur de clé doit être un protecteur de mot de passe numérique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | La méthode a réussi.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSe**</dt> <dt>1 (0x1)</dt> </dl>                                         | Stratégie de groupe n’autorise pas le stockage des informations de récupération à Active Directory.<br/>                         |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                             |
| <dl> <dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Le protecteur de clé spécifié n’est pas un protecteur de clé numérique. Vous devez entrer un protecteur de mot de passe numérique. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




