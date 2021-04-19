---
description: Supprime tous les protecteurs de clé du volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Méthode DeleteKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524678"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Méthode DeleteKeyProtectors de la \_ classe Win32 EncryptableVolume

La méthode **DeleteKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime tous les protecteurs de clé du volume.

Si un volume non chiffré possède des protecteurs de clés, lorsque **DeleteKeyProtectors** est exécuté correctement, le volume revient à un système de fichiers NTFS standard.

Si le volume n’est pas encore complètement déchiffré, utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant d’exécuter **DeleteKeyProtectors** pour vous assurer que les parties chiffrées du volume restent accessibles.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Le volume est verrouillé.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ \_Clé E \_ requise**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | Le dernier protecteur de clé pour un volume partiellement ou entièrement chiffré ne peut pas être supprimé si les protecteurs de clé sont activés. Utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer ce dernier protecteur de clé pour vous assurer que les parties chiffrées du volume restent accessibles. <br/> |
| <dl> <dt>**FVE \_ \_Limite de volume E \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Les protecteurs de clé ne peuvent pas être supprimés, car l’un d’eux est utilisé pour déverrouiller automatiquement le volume. <br/> Utilisez [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour désactiver le déverrouillage automatique avant d’exécuter cette méthode.<br/>                                                       |



 

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

 

 
