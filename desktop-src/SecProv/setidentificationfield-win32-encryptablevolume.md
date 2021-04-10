---
description: Définit la chaîne d’identificateur spécifiée dans les métadonnées du volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Méthode SetIdentificationField de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868190"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Méthode SetIdentificationField de la \_ classe Win32 EncryptableVolume

La méthode **SetIdentificationField** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) définit la chaîne d’identificateur spécifiée dans les métadonnées du volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IdentificationField* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie le champ d’identification affecté au volume. Si la chaîne facultative est absente, les valeurs du jeu de Registre sont utilisées. Si la chaîne est présente et n’est pas vide, la valeur spécifiée est utilisée. Le paramètre *IdentificationField* n’est pas sensible à la casse.

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

 

 




