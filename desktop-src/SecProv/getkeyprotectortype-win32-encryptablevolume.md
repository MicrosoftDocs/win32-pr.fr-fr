---
description: Indique le type d’un protecteur de clé donné.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Méthode GetKeyProtectorType de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529787"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyProtectorType de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyProtectorType** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique le type d’un protecteur de clé donné.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*KeyProtectorType* \[ à\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui spécifie le type du protecteur de clé.



| Valeur                                                                         | Signification                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Inconnu ou autre type de protecteur<br/>           |
| <dl> <dt>1</dt> </dl>  | Module de plateforme sécurisée<br/>             |
| <dl> <dt>2</dt> </dl>  | Clé externe<br/>                              |
| <dl> <dt>3</dt> </dl>  | Mot de passe numérique<br/>                        |
| <dl> <dt>4</dt> </dl>  | TPM et code confidentiel<br/>                               |
| <dl> <dt>5</dt> </dl>  | TPM et clé de démarrage<br/>                       |
| <dl> <dt>6</dt> </dl>  | TPM et clé de démarrage<br/>               |
| <dl> <dt>7</dt> </dl>  | Clé publique<br/>                                |
| <dl> <dt>8</dt> </dl>  | Passphrase<br/>                                |
| <dl> <dt>9</dt> </dl>  | Certificat TPM<br/>                           |
| <dl> <dt>10</dt> </dl> | Protecteur CNG (CryptoAPI Next Generation)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/>                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un *KeyProtectorType* valide.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>  |



 

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

 

 
