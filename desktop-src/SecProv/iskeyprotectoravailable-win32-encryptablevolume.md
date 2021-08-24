---
description: Indique si les protecteurs sont disponibles pour le volume.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Méthode IsKeyProtectorAvailable de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8991d6b111efbcd94ee21414d1ffd899a1890f942d6b3c5d207c8092a817ad8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667349"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>Méthode IsKeyProtectorAvailable de la \_ classe Win32 EncryptableVolume

La méthode **IsKeyProtectorAvailable** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si des protecteurs sont disponibles pour le volume.

Si un type de protecteur est fourni, la méthode indique si les protecteurs du type spécifié sont disponibles pour le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*KeyProtectorType* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui indique le type de protecteur de clé de volume interrogé.

Si ce paramètre n’est pas spécifié, tous les protecteurs de clés disponibles du volume sont interrogés.



| Valeur                                                                         | Signification                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tous les types.<br/> Tous les protecteurs de clé sont interrogés.<br/> |
| <dl> <dt>1</dt> </dl>  | Module de plateforme sécurisée (TPM) (TPM).<br/>                        |
| <dl> <dt>2</dt> </dl>  | Clé externe.<br/>                                         |
| <dl> <dt>3</dt> </dl>  | Mot de passe numérique.<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM et code confidentiel.<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM et clé de démarrage.<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM et code confidentiel et clé de démarrage.<br/>                          |
| <dl> <dt>7</dt> </dl>  | Clé publique.<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Risquent.<br/>                                           |
| <dl> <dt>9</dt> </dl>  | Certificat TPM<br/>                                       |
| <dl> <dt>10</dt> </dl> | Identificateur de sécurité (SID)<br/>                             |



 

</dd> <dt>

*IsKeyProtectorAvailable* \[ à\]
</dt> <dd>

Type : **booléen**

Valeur booléenne qui indique si un protecteur de clé de volume du type spécifié existe sur le volume.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                         | Description                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                         | La méthode a réussi.<br/>                                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | Le paramètre *KeyProtectorType* est spécifié, mais ne fait pas référence à un type de protecteur de clé valide.<br/> |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



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

 

 
