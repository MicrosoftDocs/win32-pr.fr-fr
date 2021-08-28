---
description: Fournit des informations d’État sur un test matériel d’un volume de système d’exploitation entièrement déchiffré.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Méthode GetHardwareTestStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 32d0d477459dbc7352d1d8f6779c5c76cfbd537d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475355"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Méthode GetHardwareTestStatus de la \_ classe Win32 EncryptableVolume

La méthode **GetHardwareTestStatus** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fournit des informations d’État sur un test matériel d’un volume de système d’exploitation entièrement déchiffré.

Utilisez cette méthode pour indiquer si un test matériel est en attente, ainsi que la réussite ou l’échec d’un test matériel qui s’est terminé lors du dernier redémarrage de l’ordinateur. Pour demander un test matériel, utilisez la méthode [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TestStatus* \[ à\]
</dt> <dd>

Type : **UInt32**

Spécifie si un test matériel est en attente, ainsi que la réussite de l’échec d’un test matériel qui s’est terminé lors du dernier redémarrage de l’ordinateur.




| Valeur | Signification | 
|-------|---------|
| <span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl><dt><strong>NotFailed_and_NonePending</strong></dt><dt>0</dt></dl> | Si un test a été demandé, le test a réussi au dernier redémarrage de l’ordinateur et le chiffrement du volume est maintenant en cours. Pour connaître l’état du chiffrement, consultez la méthode <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> . Dans le cas contraire, aucun test n’a été exécuté au dernier redémarrage de l’ordinateur et aucun n’est en attente. <br /> | 
| <span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl><dt><strong>Échec</strong></dt><dt>1</dt></dl> | Le chiffrement de volume n’a pas démarré. Tous les protecteurs de clé ont été supprimés.<br /> Pour résoudre un échec de test :<br /><ul><li>Consultez les informations contenues dans le paramètre <em>TestError</em> .</li><li>Ajoutez des protecteurs de clé et réutilisez la méthode <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</li></ul> | 
| <span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl><dt><strong>En attente</strong></dt><dt>2</dt></dl> | Un test a été demandé et s’exécutera au prochain redémarrage de l’ordinateur.<br /> | 




 

</dd> <dt>

*TestError* \[ à\]
</dt> <dd>

Type : **UInt32**

Spécifie l’erreur du dernier test matériel effectué.



| Valeur                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Aucune erreur ne s’est produite ou aucun test matériel n’a été exécuté lors du dernier redémarrage de l’ordinateur.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | FVE \_ E \_ keyfile \_ \_ introuvable<br/> Un lecteur flash USB avec un fichier de clé externe est introuvable. Si le problème persiste, l’ordinateur ne peut pas lire les lecteurs USB lors du redémarrage. Vous ne pourrez peut-être pas utiliser de clés externes pour déverrouiller le volume du système d’exploitation lors du redémarrage.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ keyfile \_ non valide<br/> Le fichier de clé externe sur le disque mémoire flash USB est endommagé. Essayez d’utiliser un autre lecteur flash USB pour stocker le fichier de clé externe.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ désactivé<br/> Le module de plateforme sécurisée est désactivé ou désactivé, ou désactivé et désactivé. Pour activer le module de plateforme sécurisée, utilisez le fournisseur WMI [**\_ TPM Win32**](win32-tpm.md) ou exécutez le composant logiciel enfichable de gestion du module de plateforme sécurisée (TPM. msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | \_PCR FVE E \_ TPM \_ non valide \_<br/> Le module de plateforme sécurisée a détecté une modification des services de redémarrage du système d’exploitation dans le profil de validation de plateforme actuel. Retirez un CD ou un DVD de démarrage de l’ordinateur. Si le problème persiste, vérifiez que les mises à niveau du microprogramme et du BIOS les plus récentes sont installées, et que le module de plateforme sécurisée fonctionne normalement.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | \_ \_ code PIN E FVE \_ non valide<br/> Le code PIN fourni est incorrect.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                  | Description                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | S_OK<br/> |
| <dl> <dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Le volume est verrouillé.<br/> |



 

## <a name="remarks"></a>Remarques

Pour demander un test matériel, utilisez la méthode [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

Pour exécuter un test matériel lorsque son état est en attente, procédez comme suit :

1.  Insérez dans l’ordinateur un lecteur flash USB qui contient un fichier de clé externe. Cette étape s’applique uniquement si le volume a un protecteur de clé de type « clé externe » ou « TPM et clé de démarrage ».
2.  Redémarrez l'ordinateur. Lors du redémarrage de l’ordinateur, le test matériel s’exécute automatiquement.

Pour annuler le test matériel, utilisez la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) .

Un test réussi détermine que :

-   Le module de plateforme sécurisée peut déverrouiller le volume s’il en existe un.
-   L’ordinateur peut lire un lecteur flash USB qui contient un fichier de clé externe au démarrage si le volume peut être déverrouillé par une clé externe (y compris une clé de démarrage).

Les résultats des tests matériels ne seront pas disponibles après toute modification apportée à la conversion ou après le prochain redémarrage de l’ordinateur. Consultez le journal des événements système pour obtenir des informations sur les tests matériels précédemment exécutés sur l’ordinateur.

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

 

 
