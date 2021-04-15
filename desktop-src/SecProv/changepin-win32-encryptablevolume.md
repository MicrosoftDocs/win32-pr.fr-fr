---
description: Modifie le code confidentiel associé à un volume chiffré.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Méthode ChangePIN de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525695"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Méthode ChangePIN de la \_ classe Win32 EncryptableVolume

La méthode **ChangePIN** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifie le code confidentiel associé à un volume chiffré. Si la stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est activée, un code confidentiel peut contenir des lettres, des symboles et des espaces, en plus des nombres.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*NewPIN* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne d’identification personnelle spécifiée par l’utilisateur. Cette chaîne doit être composée d’une séquence de 4 à 20 chiffres ou, si la stratégie de groupe « autoriser les codes confidentiels améliorés pour le démarrage » est activée, de 4 à 20 lettres, de symboles, d’espaces ou de nombres.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Un CD/DVD de démarrage est détecté sur cet ordinateur. Retirez le CD/DVD et redémarrez l’ordinateur.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ caractères pin non valides**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | Le paramètre *NewPIN* contient des caractères qui ne sont pas valides. Lorsque l’stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est désactivée, seuls les nombres sont pris en charge.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>     | Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ». Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Longueur de \_ \_ code confidentiel \_ non valide pour la stratégie E**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | Le paramètre *NewPIN* fourni comporte plus de 20 caractères, moins de 4 caractères, ou une longueur inférieure à la longueur minimale spécifiée par stratégie de groupe.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>        | Le protecteur de clé fourni n’existe pas sur le volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Aucun Module de plateforme sécurisée (TPM) compatible (TPM) n’a été trouvé sur cet ordinateur.<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Notes

La méthode **ChangePIN** crée un nouveau module de plateforme sécurisée et un protecteur de code confidentiel basés sur les informations de protecteur existantes et le code PIN nouvellement fourni. Le nouveau protecteur aura le même GUID. La méthode **ChangePIN** peut également être appelée pour modifier le code confidentiel d’un protecteur de clé qui utilise un code confidentiel, par exemple TPM et pin ou TPM avec pin et USB.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
