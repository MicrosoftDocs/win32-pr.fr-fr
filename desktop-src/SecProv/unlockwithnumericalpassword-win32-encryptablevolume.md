---
description: Utilise un mot de passe numérique fourni pour accéder au contenu d’un volume de données.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Méthode UnlockWithNumericalPassword de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862274"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Méthode UnlockWithNumericalPassword de la \_ classe Win32 EncryptableVolume

La méthode **UnlockWithNumericalPassword** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise un mot de passe numérique fourni pour accéder au contenu d’un volume de données.

La clé de chiffrement du volume doit avoir été sécurisée avec un ou plusieurs protecteurs de clé du type « mot de passe numérique » (à l’aide de la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) pour pouvoir déverrouiller le volume avec cette méthode.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumericalPassword* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie le mot de passe numérique.

Le mot de passe numérique doit contenir 48 chiffres. Ces chiffres peuvent être divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe. Chaque groupe de 6 chiffres doit être divisible par 11 et doit être inférieur à 65536. En supposant qu’un groupe de six chiffres s’intitule x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé comme-x1 + x2 – x3 + x4 – x5 Mod 11.

Les groupes de chiffres peuvent éventuellement être séparés par un espace ou un trait d’Union. Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » ou « xxxxxx XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX » peut également contenir des mots de passe numériques valides.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Si le volume est déjà déverrouillé et qu’aucune autre erreur ne se produit, cette méthode retourne 0.



| Code/valeur de retour                                                                                                                                                                             | Description                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | La méthode a réussi.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | Le volume n’a pas de protecteur de clé du type « mot de passe numérique ».<br/> Le format du paramètre *NumericalPassword* est valide, mais vous ne pouvez pas utiliser un mot de passe numérique pour déverrouiller le volume.<br/>           |
| <dl> <dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | Le paramètre *NumericalPassword* ne peut pas déverrouiller le volume.<br/> Un ou plusieurs protecteurs de clé du type « mot de passe numérique » existent, mais le paramètre *NumericalPassword* spécifié ne peut pas déverrouiller le volume.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ format de mot de passe non valide**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | Le format du paramètre *NumericalPassword* n’est pas valide.<br/>                                                                                                                                                     |



 

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

 

 
