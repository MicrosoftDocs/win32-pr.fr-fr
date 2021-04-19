---
description: Valide l’identificateur d’objet (OID) d’utilisation améliorée de la clé (EKU) du certificat fourni.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Méthode ProtectKeyWithCertificateThumbprint de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536767"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithCertificateThumbprint de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithCertificateThumbprint** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) valide l' [*identificateur d’objet*](../secgloss/o-gly.md) (EKU) d’utilisation améliorée de la clé du certificat fourni.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, le paramètre *FriendlyName* est créé en utilisant le nom d’objet dans le certificat.

</dd> <dt>

*CertThumbprint* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie l’empreinte numérique du certificat.

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie de façon unique le protecteur de clé créé qui peut être utilisé pour gérer ce protecteur de clé.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | La méthode a réussi.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**Erreur \_ \_Données non valides**</dt> <dt>13 (0xD)</dt> </dl>                                           | Les données ne sont pas correctes.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID NON-BitLocker**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | L’attribut EKU du certificat spécifié ne permet pas de l’utiliser pour Chiffrement de lecteur BitLocker. BitLocker ne requiert pas qu’un certificat ait un attribut EKU, mais s’il est configuré, il doit être défini sur un OID qui correspond à l’OID configuré pour BitLocker.<br/> |
| <dl> <dt>**FVE \_ \_Certificat d’utilisateur de stratégie E \_ \_ \_ non \_ autorisé**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Stratégie de groupe n’autorise pas l’utilisation de certificats d’utilisateur, tels que des cartes à puce, avec BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ Le certificat de l’utilisateur de la \_ stratégie E \_ \_ \_ doit \_ être \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Stratégie de groupe nécessite que vous fournissiez une carte à puce pour utiliser BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ La \_ stratégie E \_ interdit \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Stratégie de groupe n’autorise pas l’utilisation de certificats auto-signés.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

Si l’OID ne correspond pas à celui associé au contrôleur de service dans le registre, cette méthode échoue. Cela empêche l’utilisateur de définir les protecteurs de l’agent de récupération de données (DRA) manuellement sur le volume. Les DRA ne sont définies que par le service.

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

 

 
