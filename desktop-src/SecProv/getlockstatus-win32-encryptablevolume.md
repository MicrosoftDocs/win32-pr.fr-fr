---
description: Indique si le contenu du volume est accessible à partir de Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Méthode GetLockStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: caa213dbebc7db07851bc8df41b5d9379d3dfe97ee207f9b2578b0567fd9b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892015"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Méthode GetLockStatus de la \_ classe Win32 EncryptableVolume

La méthode **GetLockStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le contenu du volume est accessible à partir de Windows.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LockStatus* \[ à\]
</dt> <dd>

Type : **UInt32**

Spécifie si le contenu du volume est accessible à partir de Windows.



| Valeur                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Déverrouillé**</dt> <dt>0</dt> </dl> | Pour un disque dur standard :<br/> Le contenu complet du volume est accessible. Un volume déverrouillé est soit entièrement déchiffré, soit la clé de chiffrement est disponible en clair sur le disque. le volume contenant le système d’exploitation en cours d’exécution (par exemple, le volume Windows en cours d’exécution) est toujours accessible et ne peut pas être verrouillé.<br/> Pour un EHDD :<br/> La bande est déverrouillée de façon perpétuelle.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Verrouillé**</dt> <dt>1</dt> </dl>         | Pour un disque dur standard :<br/> La totalité ou une partie du contenu du volume n’est pas accessible. Un volume verrouillé doit être partiellement ou entièrement chiffré et sa clé de chiffrement ne doit pas être disponible en clair sur le disque.<br/> Pour un EHDD :<br/> La bande est déverrouillée ou verrouillée.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

Utilisez [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) et [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) pour accéder au contenu du volume. Utilisez la méthode [**Lock**](lock-win32-encryptablevolume.md) pour abandonner l’accès au contenu du volume.

Le volume qui contient le système d’exploitation en cours d’exécution est toujours accessible et ne peut pas être verrouillé.

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

 

 
