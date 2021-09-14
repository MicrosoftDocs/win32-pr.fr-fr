---
description: Répertorie les protecteurs utilisés pour sécuriser la clé de chiffrement du volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Méthode GetKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237401"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyProtectors de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) répertorie les protecteurs utilisés pour sécuriser la clé de chiffrement du volume. Si un type de protecteur est fourni, seuls les protecteurs de clé de volume du type spécifié sont retournés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyProtectorType* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui spécifie le type de protecteur de clé à retourner.

Si ce paramètre n’est pas spécifié, tous les protecteurs de clé disponibles du volume sont retournés.



| Valeur                                                                         | Signification                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tous les types.<br/> Tous les protecteurs de clé sont retournés.<br/> |
| <dl> <dt>1</dt> </dl>  | Module de plateforme sécurisée (TPM) (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Clé externe.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Mot de passe numérique.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM et code confidentiel.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM et clé de démarrage.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM et code confidentiel et clé de démarrage.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Clé publique.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Risquent.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificat TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | Identificateur de sécurité (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de chaînes qui identifient les protecteurs de clé utilisés pour sécuriser la clé de chiffrement du volume.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Le paramètre *VolumeKeyProtectorID* est spécifié, mais ne fait pas référence à un *KeyProtectorType* valide.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                   |



 

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



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

 

 
