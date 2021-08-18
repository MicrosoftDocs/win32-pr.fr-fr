---
description: Utilise le fichier de certificat fourni pour obtenir la clé dérivée et déverrouiller le volume chiffré.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Méthode UnlockWithCertificateFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004227"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Méthode UnlockWithCertificateFile de la \_ classe Win32 EncryptableVolume

La méthode **UnlockWithCertificateFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise le fichier de [*certificat*](../secgloss/c-gly.md) fourni pour obtenir la clé dérivée et déverrouiller le volume chiffré.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne qui spécifie l’emplacement et le nom du fichier. cer utilisé pour récupérer l’empreinte numérique du certificat. un certificat de [*chiffrement*](../secgloss/e-gly.md) doit être exporté au format. cer [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) binaire encodé [*x. 509*](../secgloss/x-gly.md) ou Base-64 encodé x. 509. Le certificat de chiffrement peut être généré à partir de l’infrastructure PKI de Microsoft, d’une infrastructure à clé publique tierce ou auto-signé.

</dd> <dt>

*Code confidentiel* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chaîne d’identification personnelle spécifiée par l’utilisateur. Cette chaîne doit être composée d’une séquence de 4 à 20 chiffres. Cette chaîne est utilisée pour authentifier silencieusement le [*fournisseur de stockage de clés*](../secgloss/k-gly.md) (KSP) lorsqu’il est utilisé avec une [*carte à puce*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | La méthode a réussi.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**Erreur \_ FICHIER \_ \_ introuvable**</dt> <dt>0000000002 (0X2)</dt> </dl>                 | Le système ne peut pas fichier le fichier spécifié.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Le volume ne peut pas être déverrouillé avec les informations fournies. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Le protecteur de clé fourni n’existe pas sur le volume. Vous devez entrer un autre protecteur de clé.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ Échec de l' \_ \_ authentification \_ PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | La [*clé privée*](../secgloss/p-gly.md), associée au certificat spécifié, n’a pas pu être autorisée. L’autorisation de clé privée n’a pas été fournie ou l’autorisation fournie n’était pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



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

 

 
