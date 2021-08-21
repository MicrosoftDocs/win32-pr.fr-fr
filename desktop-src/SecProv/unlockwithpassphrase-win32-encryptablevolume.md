---
description: Méthode UnlockWithPassphrase de la classe Win32_EncryptableVolume-utilise la phrase secrète pour obtenir la clé dérivée.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Méthode UnlockWithPassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004167"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Méthode UnlockWithPassphrase de la \_ classe Win32 EncryptableVolume

La méthode **UnlockWithPassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la phrase secrète pour obtenir la clé dérivée. Une fois la clé dérivée calculée, la clé dérivée est utilisée pour déverrouiller la clé principale du volume chiffré.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Phrase secrète* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie la phrase secrète.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                       | Description                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | La méthode a réussi.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ empêche la \_ phrase secrète**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | Le paramètre de stratégie de groupe qui requiert la conformité FIPS a empêché la création ou l’utilisation de la phrase secrète. <br/> |
| <dl> <dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La phrase secrète fournie ne répond pas aux exigences de longueur minimale ou maximale.<br/>                              |
| <dl> <dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La phrase secrète ne respecte pas les exigences de complexité définies par l’administrateur dans la stratégie de groupe.<br/>             |
| <dl> <dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | Le volume ne peut pas être déverrouillé avec les informations fournies. <br/>                                                  |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | Le protecteur de clé fourni n’existe pas sur le volume. Vous devez entrer un autre protecteur de clé.<br/>                 |



 

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

 

 




