---
description: Écrit la clé externe associée au protecteur de clé de volume spécifié dans un fichier système, masqué et en lecture seule dans le dossier spécifié.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Méthode SaveExternalKeyToFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529306"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Méthode SaveExternalKeyToFile de la \_ classe Win32 EncryptableVolume

La méthode **SaveExternalKeyToFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) écrit la clé externe associée au protecteur de clé de volume spécifié dans un fichier système, masqué et en lecture seule dans le dossier spécifié.

Cette méthode s’applique uniquement aux protecteurs de clés du type « clé externe » ou « TPM et clé de démarrage ».

## <a name="syntax"></a>Syntaxe


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui contient l’emplacement du volume ou du dossier où la clé externe associée au protecteur de clé spécifié doit être enregistrée. Ce chemin d’accès n’inclut pas le nom du fichier, qui est interne et peut changer d’une version à l’autres. Utilisez **GetExternalKeyFileName** pour récupérer le nom du fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                   | Description                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | La méthode a réussi.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | Le volume est verrouillé.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « clé externe » ou « TPM et clé de démarrage ».<br/>            |
| <dl> <dt>**Erreur \_ Chemin d’accès \_ \_ introuvable**</dt> <dt>2147942403 (0x80070003)</dt> </dl> | Le paramètre *path* ne fait pas référence à un emplacement valide.<br/> Assurez-vous que le nom de fichier n’est pas inclus dans le paramètre *path* .<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                      |



 

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

 

 
