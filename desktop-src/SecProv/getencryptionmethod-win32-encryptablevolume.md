---
description: Indique l’algorithme de chiffrement et la taille de clé utilisés sur le volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Méthode GetEncryptionMethod de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008998"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Méthode GetEncryptionMethod de la \_ classe Win32 EncryptableVolume

La méthode **GetEncryptionMethod** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indique l’algorithme de chiffrement et la taille de clé utilisés sur le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncryptionMethod* \[ à\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui spécifie l’algorithme de chiffrement et la taille de clé utilisés sur le volume.



| Valeur                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Aucun**</dt> <dt>0</dt> </dl>                                | Le volume n’est pas chiffré.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ avec \_ diffuseur**</dt> <dt>1</dt> </dl> | Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche de diffuseurs, avec une taille de clé AES de 128 bits. cette méthode n’est plus disponible sur les appareils exécutant Windows 8.1 ou une version ultérieure.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ avec \_ diffuseur**</dt> <dt>2</dt> </dl> | Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche de diffuseurs, avec une taille de clé AES de 256 bits. cette méthode n’est plus disponible sur les appareils exécutant Windows 8.1 ou une version ultérieure.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES), avec une taille de clé AES de 128 bits.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES), avec une taille de clé AES de 256 bits.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**Matériel \_ CHIFFREment**</dt> <dt>5</dt> </dl>         | Le volume a été entièrement ou partiellement chiffré à l’aide des fonctionnalités matérielles du lecteur.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | Le volume a été entièrement ou partiellement chiffré avec XTS à l’aide de l’Advanced Encryption Standard (AES) et une taille de clé AES de 128 bits. cette méthode est disponible uniquement sur les appareils exécutant Windows 10, version 1511 ou ultérieure.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | Le volume a été entièrement ou partiellement chiffré avec XTS à l’aide de l’Advanced Encryption Standard (AES) et une taille de clé AES de 256 bits. cette méthode est disponible uniquement sur les appareils exécutant Windows 10, version 1511 ou ultérieure.<br/>                          |
| <dl> <dt>(UInt32)-1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> Le volume a été entièrement ou partiellement chiffré avec un algorithme et une taille de clé inconnus.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ à\]
</dt> <dd>

Type : **chaîne**

L’algorithme de chiffrement est configuré sur le lecteur à chiffrement automatique. Une chaîne NULL signifie que BitLocker utilise le chiffrement logiciel ou qu’aucune méthode de chiffrement n’est signalée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



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

 

 
