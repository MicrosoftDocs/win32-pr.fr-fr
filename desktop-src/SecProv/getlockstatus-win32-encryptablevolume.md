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
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514805"
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
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Déverrouillé**</dt> <dt>0</dt> </dl> | Pour un disque dur standard :<br/> Le contenu complet du volume est accessible. Un volume déverrouillé est soit entièrement déchiffré, soit la clé de chiffrement est disponible en clair sur le disque. Le volume contenant le système d’exploitation en cours d’exécution (par exemple, le volume Windows en cours d’exécution) est toujours accessible et ne peut pas être verrouillé.<br/> Pour un EHDD :<br/> La bande est déverrouillée de façon perpétuelle.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Verrouillé**</dt> <dt>1</dt> </dl>         | Pour un disque dur standard :<br/> La totalité ou une partie du contenu du volume n’est pas accessible. Un volume verrouillé doit être partiellement ou entièrement chiffré et sa clé de chiffrement ne doit pas être disponible en clair sur le disque.<br/> Pour un EHDD :<br/> La bande est déverrouillée ou verrouillée.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Utilisez [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) et [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) pour accéder au contenu du volume. Utilisez la méthode [**Lock**](lock-win32-encryptablevolume.md) pour abandonner l’accès au contenu du volume.

Le volume qui contient le système d’exploitation en cours d’exécution est toujours accessible et ne peut pas être verrouillé.

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

 

 
