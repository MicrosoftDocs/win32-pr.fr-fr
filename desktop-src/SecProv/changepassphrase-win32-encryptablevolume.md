---
description: Utilise la nouvelle phrase secrète pour obtenir une nouvelle clé dérivée.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Méthode ChangePassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523343"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Méthode ChangePassphrase de la \_ classe Win32 EncryptableVolume

La méthode **ChangePassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la nouvelle phrase secrète pour obtenir une nouvelle clé dérivée. Une fois la clé dérivée calculée, la nouvelle clé dérivée est utilisée pour sécuriser la clé principale du volume chiffré.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*NewPassphrase* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne mise à jour qui spécifie la phrase secrète.

</dd> <dt>

*NewProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique mis à jour, utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                       | Description                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | La méthode a réussi.<br/>                                                                                  |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Le volume est déjà verrouillé par Chiffrement de lecteur BitLocker. Vous devez déverrouiller le lecteur à partir du panneau de configuration.<br/>   |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                           |
| <dl> <dt>**FVE \_ E \_ \_ mise à jour**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                  | Le bloc de contrôle du volume chiffré a été mis à jour par un autre thread.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>            | Le type de protecteur de clé spécifié n’est pas correct. <br/>                                                    |
| <dl> <dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La phrase secrète mise à jour fournie ne répond pas aux exigences de longueur minimale ou maximale. <br/>                  |
| <dl> <dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La phrase secrète mise à jour ne répond pas aux exigences de complexité définies par l’administrateur dans la stratégie de groupe. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




