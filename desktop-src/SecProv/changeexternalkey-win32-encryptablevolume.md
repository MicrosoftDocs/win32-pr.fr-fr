---
description: Modifie une clé externe qui est associée à un volume chiffré.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Méthode ChangeExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529360"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Méthode ChangeExternalKey de la \_ classe Win32 EncryptableVolume

La méthode **ChangeExternalKey** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifie une clé externe qui est associée à un volume chiffré.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

 *NewExternalKey* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume.

</dd> <dt>

*NewVolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique mis à jour qui est utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | Le paramètre *NewExternalKey* n’est pas un tableau de taille 32.<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>          | Un CD/DVD de démarrage est détecté sur cet ordinateur. Retirez le CD/DVD et redémarrez l’ordinateur.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Le protecteur de clé fourni n’existe pas sur le volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ». Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être utilisée pour modifier la clé externe pour tout protecteur de clé qui utilise une clé externe.

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

 

 




