---
description: Utilise une clé externe fournie pour accéder au contenu d’un volume de données.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Méthode UnlockWithExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536613"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Méthode UnlockWithExternalKey de la \_ classe Win32 EncryptableVolume

La méthode **UnlockWithExternalKey** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise une clé externe fournie pour accéder au contenu d’un volume de données.

La clé de chiffrement du volume doit avoir été sécurisée avec un ou plusieurs protecteurs de clé du type « clé externe » à l’aide de la méthode [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour pouvoir déverrouiller le volume avec cette méthode.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ExternalKey* \[ dans\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume. Cette clé peut être obtenue en appelant la méthode [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si le volume est déjà déverrouillé, cette méthode retourne 0.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                                                                       |
| <dl> <dt>**Erreur \_ Aucune valeur donnée n' \_ a été trouvée**</dt> <dt>(0x)</dt> </dl>          | Le volume n’a pas de protecteur de clé du type « clé externe ».<br/>                                                             |
| <dl> <dt>**Erreur \_ \_Mot de passe non valide**</dt> - <dt>aucune valeur donnée (0x)</dt> </dl>   | Un ou plusieurs protecteurs de clé du type « clé externe » existent, mais le paramètre *ExternalKey* spécifié ne peut pas déverrouiller le volume.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Le paramètre *ExternalKey* n’est pas un tableau de taille 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                |



 

## <a name="remarks"></a>Notes

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

 

 
