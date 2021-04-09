---
description: Retourne la chaîne d’identificateur disponible dans les métadonnées du volume.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Méthode GetIdentificationField de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112638"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Méthode GetIdentificationField de la \_ classe Win32 EncryptableVolume

La méthode **GetIdentificationField** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la chaîne d’identificateur disponible dans les métadonnées du volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IdentificationField* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie le champ d’identification affecté au volume.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Ce lecteur est verrouillé par Chiffrement de lecteur BitLocker. Vous devez déverrouiller ce volume à partir du panneau de configuration. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                    |



 

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

 

 




