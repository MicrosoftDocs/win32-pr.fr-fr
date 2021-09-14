---
description: Méthode ProtectKeyWithPassphrase de la classe Win32_EncryptableVolume-utilise la phrase secrète pour obtenir la clé dérivée.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Méthode ProtectKeyWithPassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008983"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithPassphrase de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithPassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la phrase secrète pour obtenir la clé dérivée. Une fois la clé dérivée calculée, la clé dérivée est utilisée pour sécuriser la clé principale du volume chiffré.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.

</dd> <dt>

*Phrase secrète* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie la phrase secrète.

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie de façon unique le protecteur de clé créé.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                        | Description                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | La méthode a réussi.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ non \_ autorisé \_ en \_ \_ mode sans échec**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Chiffrement de lecteur BitLocker ne peut être utilisé qu’à des fins de récupération lorsqu’il est utilisé en Mode Coffre.<br/>                     |
| <dl> <dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ non \_ autorisée**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | La stratégie de groupe n’autorise pas la création d’une phrase secrète.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ empêche la \_ phrase secrète**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | Le paramètre de stratégie de groupe qui requiert la conformité FIPS a empêché la création ou l’utilisation de la phrase secrète.<br/> |
| <dl> <dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | La phrase secrète fournie ne répond pas aux exigences de longueur minimale ou maximale.<br/>                             |
| <dl> <dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | La phrase secrète ne respecte pas les exigences de complexité définies par l’administrateur dans la stratégie de groupe.<br/>            |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Le volume est déjà verrouillé par Chiffrement de lecteur BitLocker. Vous devez déverrouiller le lecteur à partir du panneau de configuration.<br/>     |
| <dl> <dt>**FVE \_ E \_ \_ mise à jour**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Le bloc de contrôle du volume chiffré a été mis à jour par un autre thread.<br/>                                     |
| <dl> <dt>**FVE \_ Le \_ protecteur de clé E \_ n’est \_ pas \_ pris en charge**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | Le protecteur de clé n’est pas pris en charge par la version de Chiffrement de lecteur BitLocker actuellement sur le volume.<br/>      |
| <dl> <dt>**FVE \_ \_Phrase secrète du volume du système d’exploitation \_ \_ \_ non \_ autorisée**</dt> <dt>2150695021 (0x8031006D)</dt> </dl> | La phrase secrète ne peut pas être ajoutée au volume du système d’exploitation. <br/>                                               |
| <dl> <dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | Le protecteur de clé fourni existe déjà sur ce volume.<br/>                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise, Windows 7 Édition Intégrale des \[ applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




