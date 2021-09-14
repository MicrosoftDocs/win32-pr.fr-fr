---
description: Sécurise la clé de chiffrement du volume à l’aide d’une clé externe 256 bits.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Méthode ProtectKeyWithExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008988"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithExternalKey de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithExternalKey** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide d’une clé externe 256 bits. Cette clé externe peut être utilisée pour récupérer des échecs d’authentification d’autres protecteurs de clé (par exemple, TPM).

Utilisez la méthode [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) pour enregistrer cette clé externe dans un fichier. Les périphériques de mémoire USB qui contiennent cette clé externe peuvent être utilisés comme clé de démarrage ou clé de récupération au démarrage de l’ordinateur.

Un protecteur de clé de type « clé externe » est créé pour le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie un identificateur affecté à l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.

</dd> <dt>

*ExternalKey* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume.

Si aucune clé externe n’est spécifiée, une clé est générée de façon aléatoire. Utilisez la méthode [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) pour obtenir la clé générée de façon aléatoire.

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Le paramètre *ExternalKey* est fourni, mais n’est pas un tableau de taille 4.<br/>            |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/>                                                             |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/> |



 

## <a name="remarks"></a>Remarques

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

 

 
