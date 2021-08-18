---
description: Indique l’état du chiffrement ou du déchiffrement sur le volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Méthode GetConversionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004480"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Méthode GetConversionStatus de la \_ classe Win32 EncryptableVolume

La méthode **GetConversionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique l’état du chiffrement ou du déchiffrement sur le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConversionStatus* \[ à\]
</dt> <dd>

Type : **UInt32**

État de chiffrement ou de déchiffrement du volume. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Pour un disque dur standard (HDD), le volume est entièrement déchiffré.<br/> Pour un disque dur chiffré (EHDD) matériel, le volume est déverrouillé de façon permanente.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Pour un disque dur standard (HDD), le volume est entièrement chiffré.<br/> Pour un disque dur chiffré (EHDD) matériel, le volume n’est pas déverrouillé de façon permanente.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | Le volume est partiellement chiffré.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | Le volume est partiellement chiffré.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | Le volume a été suspendu pendant la progression du chiffrement. Le volume est partiellement chiffré.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | Le volume a été suspendu pendant la progression du déchiffrement. Le volume est partiellement chiffré.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ à\]
</dt> <dd>

Type : **UInt32**

Pourcentage du volume chiffré. Il s’agit d’un entier compris entre 0 et 100 inclus.

En raison de l’arrondi des nombres, un pourcentage de chiffrement de 0 ou de 100 n’indique pas nécessairement que le disque est entièrement déchiffré ou entièrement chiffré. Utilisez toujours *ConversionStatus* pour déterminer si le disque est en fait entièrement déchiffré ou entièrement chiffré.

</dd> <dt>

*EncryptionFlags* \[ à\]
</dt> <dd>

Type : **UInt32**

Indicateurs qui décrivent le comportement de chiffrement.

Combinaison de 32 bits avec les bits suivants actuellement définis.



| Valeur                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement. Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) reprend efficacement la conversion et la valeur de ce bit est ignorée. Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu. Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Effectuez une réinitialisation à la demande de l’espace libre du volume. L’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Effectuez l’opération demandée de façon synchrone. L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue. Cet indicateur est pris en charge uniquement avec la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) . Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours. Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ à\]
</dt> <dd>

Type : **UInt32**

État d’effacement de l’espace libre. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                               | Signification                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | L’espace libre n’a pas été réinitialisé.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | L’espace libre a été réinitialisé.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | L’effacement de l’espace libre est actuellement en cours.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | L’effacement de l’espace libre a été suspendu.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ à\]
</dt> <dd>

Type : **UInt32**

Valeur comprise entre 0 et 100 qui spécifie le pourcentage d’espace libre qui a été réinitialisé.

</dd> <dt>

*PrecisionFactor* \[ dans\]
</dt> <dd>

Type : **UInt32**

Valeur comprise entre 0 et 4 qui spécifie le niveau de précision.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | La méthode a réussi.<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/>      |



 

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

 

 
