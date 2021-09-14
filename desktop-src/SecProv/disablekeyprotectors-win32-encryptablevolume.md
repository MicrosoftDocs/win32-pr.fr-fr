---
description: Désactive ou interrompt tous les protecteurs de clé associés à ce volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Méthode DisableKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222153"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Méthode DisableKeyProtectors de la \_ classe Win32 EncryptableVolume

La méthode **DisableKeyProtectors** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) désactive ou interrompt tous les protecteurs de clé associés à ce volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DisableCount* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Entier qui spécifie le nombre de redémarrages pour lesquels les protecteurs de clé seront désactivés. Ce paramètre est uniquement disponible sur les volumes du système d’exploitation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/>      |



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Cette méthode expose la clé de chiffrement du volume en clair sur le disque dur, ce qui désactive toute protection du volume. Nous vous recommandons de ne pas avoir de mot de passe ou de clé de chiffrement en texte clair.

## <a name="remarks"></a>Notes

De nouveaux protecteurs de clé peuvent être ajoutés même lorsque les protecteurs de clé sont désactivés ou suspendus. Ces protecteurs de clé restent désactivés, sauf si [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) est appelé.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
