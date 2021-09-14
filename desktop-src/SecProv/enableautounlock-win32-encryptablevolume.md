---
description: Permet de déverrouiller automatiquement un volume de données lorsque le volume est monté.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Méthode EnableAutoUnlock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222137"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Méthode EnableAutoUnlock de la \_ classe Win32 EncryptableVolume

La méthode **EnableAutoUnlock** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) permet de déverrouiller automatiquement un volume de données lorsque le volume est monté.

Le déverrouillage automatique enregistre une clé externe sur le système d’exploitation qui peut déverrouiller automatiquement le volume sur le volume du système d’exploitation en cours d’exécution.

Pour utiliser cette méthode, le volume du système d’exploitation doit déjà être protégé par Chiffrement de lecteur BitLocker ou doit avoir un chiffrement en cours. En outre, il doit déjà exister une clé externe pour le volume de données. Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer la clé externe qui peut déverrouiller automatiquement le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie le protecteur de clé du type « clé externe » utilisé pour déverrouiller automatiquement le volume.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                           | Description                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | La méthode a réussi.<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>          | Le volume est verrouillé.<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé valide du type « clé externe ».<br/>                                                          |
| <dl> <dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.<br/>                                                                                       |
| <dl> <dt>**FVE \_ E/ \_ s \_ non \_ protégé**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | La méthode ne peut pas être exécutée si le volume du système d’exploitation en cours d’exécution n’est pas protégé par Chiffrement de lecteur BitLocker ou si le chiffrement n’est pas en cours.<br/> |
| <dl> <dt> **\_ Limite du \_ volume E FVE \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Le déverrouillage automatique sur le volume a déjà été activé.<br/>                                                                                                    |



 

## <a name="remarks"></a>Notes

En fonction d’un protecteur de clé de volume valide du type « clé externe », la clé externe 256 bits associée est extraite du protecteur et stockée dans le Registre du système d’exploitation en cours d’exécution, avec l’ID de protecteur de clé de volume.

Si la clé externe associée à l’ID de protecteur de clé de volume est supprimée, la fonctionnalité de déverrouillage automatique du volume est désactivée ou suspendue.

> [!Note]  
> Le support amovible n’est pas pris en charge actuellement.

 

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
