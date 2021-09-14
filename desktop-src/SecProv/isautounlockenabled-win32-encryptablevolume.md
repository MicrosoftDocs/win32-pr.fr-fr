---
description: Indique si le volume est automatiquement déverrouillé lorsqu’il est monté.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Méthode IsAutoUnlockEnabled de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011115"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Méthode IsAutoUnlockEnabled de la \_ classe Win32 EncryptableVolume

La méthode **IsAutoUnlockEnabled** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le volume est automatiquement déverrouillé lorsqu’il est monté (par exemple, lorsque des périphériques mémoire amovibles sont connectés à l’ordinateur).

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsAutoUnlockEnabled* \[ à\]
</dt> <dd>

Type : **booléen**

Valeur booléenne qui est true si la clé externe utilisée pour déverrouiller automatiquement le volume existe et a été stockée dans le volume du système d’exploitation en cours d’exécution, sinon elle est false.

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique qui contient l’ID de protecteur de clé de volume chiffré associé si *IsAutoUnlockEnabled* a la valeur true.

Si *IsAutoUnlockEnabled* a la valeur false, *VolumeKeyProtectorID* est une chaîne vide.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                     | Description                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | La méthode a réussi.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.<br/>      |



 

## <a name="remarks"></a>Notes

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

 

 
