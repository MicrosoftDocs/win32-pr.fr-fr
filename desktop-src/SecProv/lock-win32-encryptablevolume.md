---
description: Démonte le volume et supprime la clé de chiffrement du volume de la mémoire système.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Méthode Lock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862286"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Méthode Lock de la \_ classe Win32 EncryptableVolume

La méthode **Lock** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) démonte le volume et supprime la clé de chiffrement du volume de la mémoire système. Le contenu du volume reste inaccessible jusqu’à ce qu’il soit déverrouillé par la méthode [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou par la méthode [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) . Cette méthode ne peut pas être exécutée correctement pour le volume du système d’exploitation en cours d’exécution.

> [!Note]  
> Si le disque prend en charge le chiffrement matériel, la bande est définie sur « verrouillé ».

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ForceDismount* \[ dans, facultatif\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true** , le disque est démonté de force.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                           | Description                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | La méthode a réussi.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ACCÈS \_ refusé**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Les applications accèdent à ce volume. Si tous les accès ne sont pas exclusifs, la spécification du paramètre *ForceDismount* sur true permet à la méthode de s’exécuter correctement.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ chiffré**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | Le volume est entièrement déchiffré et ne peut pas être verrouillé.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ \_Protection E \_ désactivée**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | La clé de chiffrement du volume est disponible en clair sur le disque, ce qui empêche le verrouillage du volume.<br/>                                                    |
| <dl> <dt>**FVE \_ \_Clé de récupération E \_ \_ requise**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | Le volume n’a pas de protecteurs de clé du type « mot de passe numérique » ou « clé externe » nécessaires au déverrouillage du volume.<br/>                            |



 

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

 

 
