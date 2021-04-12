---
description: Supprime un protecteur de clé donné pour le volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Méthode DeleteKeyProtector de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318206"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a>Méthode DeleteKeyProtector de la \_ classe Win32 EncryptableVolume

La méthode **DeleteKeyProtector** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) supprime un protecteur de clé donné pour le volume.

Si un volume non chiffré possède des protecteurs de clés, lorsque **DeleteKeyProtector** supprime le dernier protecteur de clé, le volume est rétabli dans un système de fichiers NTFS standard.

Si un volume n’a jamais été chiffré, le fait de supprimer le protecteur de clé sera rétabli en NTFS.

Si le volume n’est pas encore complètement déchiffré, utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer le dernier protecteur de clé du volume pour vous assurer que les parties chiffrées du volume restent accessibles.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>         | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                  | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé valide.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ \_Clé E \_ requise**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | Le dernier protecteur de clé pour un volume partiellement ou entièrement chiffré ne peut pas être supprimé si les protecteurs de clé sont activés. Utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer ce dernier protecteur de clé pour vous assurer que les parties chiffrées du volume restent accessibles. <br/> |
| <dl> <dt>**FVE \_ \_Limite de volume E \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Ce protecteur de clé ne peut pas être supprimé car il est utilisé pour déverrouiller automatiquement le volume. <br/> Utilisez [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour désactiver le déverrouillage automatique avant de supprimer ce protecteur de clé.<br/>                                                    |



 

## <a name="remarks"></a>Notes

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

 

 
