---
description: Supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Méthode DisableAutoUnlock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865434"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Méthode DisableAutoUnlock de la \_ classe Win32 EncryptableVolume

La méthode **DisableAutoUnlock** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution afin qu’un volume de données ne soit pas automatiquement déverrouillé lorsqu’il est monté, par exemple lorsque des périphériques mémoire amovibles sont connectés à l’ordinateur.

Si le déverrouillage automatique est désactivé ou suspendu, les méthodes [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) doivent être utilisées pour déverrouiller le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                       | Description                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | La méthode a réussi.<br/>                                                       |
| <dl> <dt> **\_ Volume FVE \_ E \_ non \_ lié**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | Le déverrouillage automatique sur le volume est désactivé.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.<br/>      |



 

## <a name="remarks"></a>Notes

Si aucune erreur n’est retournée, cette méthode supprime du Registre tous les ID de protecteur de volume et les clés externes utilisés pour déverrouiller automatiquement le volume.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
