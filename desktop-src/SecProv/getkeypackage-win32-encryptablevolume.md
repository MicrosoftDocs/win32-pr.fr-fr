---
description: Exporte des informations qui peuvent aider à récupérer les données chiffrées lorsque le lecteur est gravement endommagé et qu’il n’existe aucun fichier de sauvegarde de données.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Méthode GetKeyPackage de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522143"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyPackage de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyPackage** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exporte des informations qui peuvent aider à récupérer des données chiffrées lorsque le lecteur est gravement endommagé et qu’il n’existe aucun fichier de sauvegarde de données.

Les informations exportées se composent de la clé de chiffrement du volume sécurisée par un protecteur de clé du type « mot de passe numérique » ou « clé externe ». Pour utiliser ce package, vous devez également enregistrer le mot de passe numérique ou la clé externe correspondant.

> [!IMPORTANT]
> Si vous choisissez d’exporter un package de clés, veillez à conserver ces informations dans un emplacement bien protégé. Ne transmettent pas ces informations avec votre ordinateur. Si ce package de clés est perdu ou volé, vous devez déchiffrer le volume et le rechiffrer à l’aide d’une nouvelle clé.

 

En cas de défaillance d’un disque, l’outil de réparation BitLocker existe pour aider à récupérer les données disponibles. Pour plus d’informations sur la façon dont cet outil peut utiliser le package de clé, consultez [comment utiliser l’outil de réparation BitLocker pour faciliter la récupération de données à partir d’un volume chiffré dans Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré. Pour exporter un package de clés, vous devez utiliser un protecteur de clé de type « numérique de mot de passe » ou « clé externe ».

</dd> <dt>

*Keypackage \[ \]* en \[ sortie\]
</dt> <dd>

Type : **UInt8**

Flux d’octets qui contient la clé de chiffrement d’un volume, sécurisée par le protecteur de clé spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Le protecteur de clé fourni n’existe pas sur le volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ». Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.<br/> |



 

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

 

 
