---
description: Récupère la clé publique et l’empreinte de certificat d’un protecteur de clé publique.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Méthode GetKeyProtectorCertificate de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237432"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyProtectorCertificate de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyProtectorCertificate** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère la [*clé publique*](../secgloss/p-gly.md) et l’empreinte de [*certificat*](../secgloss/c-gly.md) pour un protecteur de clé publique.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*PublicKey* \[ à\]
</dt> <dd>

Type : **UInt8 \[ \]**

Tableau d’octets qui spécifie la clé publique.

</dd> <dt>

*CertThumbprint* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie l’empreinte numérique du certificat.

</dd> <dt>

*Le type* \[ à\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui spécifie le type du protecteur de clé. Cet entier permet de faire la distinction entre l’agent de récupération de données (DRA) et les certificats utilisateur.



| Valeur                                                                        | Signification                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | Le certificat est un DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | Le certificat n’est pas un DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                       | Description                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | La méthode a réussi.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | Le protecteur de clé spécifié n’est pas un protecteur de clé. Vous devez entrer un autre protecteur de clé.<br/>            |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Ce lecteur est verrouillé par Chiffrement de lecteur BitLocker. Vous devez déverrouiller ce volume à partir du panneau de configuration. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ \_Certificat d’utilisateur de stratégie E \_ \_ \_ requis**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Stratégie de groupe nécessite l’utilisation d’un certificat d’utilisateur, tel qu’une carte à puce.<br/>                           |



 

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



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

 

 
