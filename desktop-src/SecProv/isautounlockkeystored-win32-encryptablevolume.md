---
description: Indique si des clés externes ou des informations associées qui peuvent être utilisées pour déverrouiller automatiquement des volumes de données existent dans le volume du système d’exploitation en cours d’exécution.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Méthode IsAutoUnlockKeyStored de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536549"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Méthode IsAutoUnlockKeyStored de la \_ classe Win32 EncryptableVolume

La méthode **IsAutoUnlockKeyStored** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si des clés externes ou des informations associées qui peuvent être utilisées pour déverrouiller automatiquement des volumes de données existent dans le volume du système d’exploitation en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsAutoUnlockKeyStored* \[ à\]
</dt> <dd>

Type : **booléen**

La **valeur est true** si des informations pouvant être utilisées pour déverrouiller automatiquement des volumes de données sont stockées dans le Registre du volume du système d’exploitation en cours d’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                   | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | La méthode a réussi.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ OS \_ volume**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | La méthode ne peut être exécutée que pour le volume du système d’exploitation en cours d’exécution.<br/>     |



 

## <a name="remarks"></a>Notes

Utilisez [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) pour supprimer toutes les informations de déverrouillage du volume du système d’exploitation en cours d’exécution.

Les informations utilisées pour déverrouiller un volume sont stockées lors de l’exécution de [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) pour un volume de données pendant l’exécution du volume du système d’exploitation en cours d’exécution.

**IsAutoUnlockKeyStored** diffère de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) dans le cas où, même si le déverrouillage automatique est désactivé pour tous les volumes de données actuellement connectés à l’ordinateur, il se peut qu’il y ait toujours des informations de déverrouillage associées aux volumes de données déconnectés ou aux volumes de données qui n’existent plus.

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

 

 
