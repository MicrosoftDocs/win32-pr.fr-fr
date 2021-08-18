---
description: Commence le chiffrement d’un volume de système d’exploitation entièrement déchiffré après un test matériel.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Méthode EncryptAfterHardwareTest de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5365bd9aca023d42d9f2ab1d9de5d242497b8b21842004b2bb508f362752bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004497"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Méthode EncryptAfterHardwareTest de la \_ classe Win32 EncryptableVolume

La méthode **EncryptAfterHardwareTest** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) commence le chiffrement d’un volume de système d’exploitation entièrement déchiffré après un test matériel. Un redémarrage est nécessaire pour effectuer ce test matériel. Utilisez cette méthode à la place de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) pour vérifier que BitLocker fonctionnera comme prévu.

> [!Note]  
> Si le disque dur est chiffré sur le matériel, cette méthode ne chiffre pas les données. Au lieu de cela, il définit l’état de la bande sur déverrouillé de « perpétuellement déverrouillé ». Si la bande est verrouillée, déverrouillée ou est en lecture seule, le lecteur est considéré comme étant chiffré.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncryptionMethod* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Spécifie l’algorithme de chiffrement et la taille de clé utilisés pour chiffrer le volume. Laissez ce paramètre vide pour utiliser la valeur par défaut de zéro. Si le volume est partiellement ou entièrement chiffré, la valeur de ce paramètre doit être égale à 0 ou correspondre à la méthode de chiffrement existante du volume. Si le paramètre de stratégie de groupe correspondant a été activé avec une valeur valide, la valeur de ce paramètre doit être 0 ou correspondre au paramètre stratégie de groupe.

Si le paramètre de stratégie de groupe correspondant n’est pas valide, la valeur par défaut AES 128 avec diffuseur est utilisée.



| Valeur                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>0</dt> <dt>**non spécifié**</dt> </dl> | Utilisez le paramètre de stratégie de groupe actuel, s’il est disponible et valide, ou la méthode de chiffrement par défaut dans le cas contraire.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 AVEC DIFFUSEUR<br/> Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche diffuseur et en utilisant une taille de clé AES de 128 bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 AVEC DIFFUSEUR<br/> Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche diffuseur et en utilisant une taille de clé AES de 256 bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) et à l’aide d’une taille de clé AES de 128 bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) et à l’aide d’une taille de clé AES de 256 bits.<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Indicateurs qui décrivent le comportement de chiffrement.

**Windows 7, Windows server 2008 R2, Windows Vista Enterprise et Windows Server 2008 :** Ce paramètre n’est pas disponible.

Combinaison de 32 bits avec les bits suivants actuellement définis.



| Valeur                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement. Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) reprend efficacement la conversion et la valeur de ce bit est ignorée. Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou **EncryptAfterHardwareTest** démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu. Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Effectuez une réinitialisation à la demande de l’espace libre du volume. L’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Effectuez l’opération demandée de façon synchrone. L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue. Cet indicateur est pris en charge uniquement avec la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) . Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours. Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Cette méthode est retournée immédiatement. Si le volume est déjà entièrement chiffré et qu’aucune autre erreur n’est retournée, cette méthode retourne zéro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code/valeur de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </dl></td>
<td>La méthode a réussi.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>Le paramètre <em>EncryptionMethod</em> est fourni, mais il n’est pas dans la plage connue ou ne correspond pas au paramètre de stratégie de groupe actuel.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Il n’existe aucune clé de chiffrement pour le volume.<br/> Désactivez les protecteurs de clé à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> , ou utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Le volume ne peut pas être chiffré car cet ordinateur est configuré pour faire partie d’un cluster de serveurs.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </dl></td>
<td>Aucun protecteur de clé de type &quot; TPM &quot; , &quot; TPM et pin &quot; , TPM, &quot; code confidentiel et clé de démarrage &quot; , TPM et clé de &quot; démarrage &quot; ou &quot; clé externe ne &quot; peut être trouvé. Le test matériel concerne uniquement les protecteurs de clé précédents.<br/> Si vous souhaitez toujours exécuter un test matériel, vous devez utiliser l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>Le volume est partiellement ou entièrement chiffré.<br/> Le test matériel s’applique avant le chiffrement. Si vous souhaitez toujours exécuter le test, utilisez d’abord la méthode <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> , puis utilisez l’une des méthodes suivantes pour ajouter des protecteurs de clé :
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>Le volume est un volume de données.<br/> Le test matériel s’applique uniquement aux volumes qui peuvent démarrer le système d’exploitation. Exécutez cette méthode sur le volume du système d’exploitation actuellement démarré.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Aucun protecteur de clé du type de &quot; mot de passe numérique &quot; n’est spécifié. Le stratégie de groupe nécessite une sauvegarde des informations de récupération pour Active Directory Domain Services. Pour ajouter au moins un protecteur de clé de ce type, utilisez la méthode <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

lorsque vous utilisez cette méthode sans le second paramètre facultatif (selon la définition de la Windows 7 et Windows Vista Enterprise), la méthode lance toujours la conversion en mode complet afin de conserver un comportement à compatibilité descendante. de cette façon, l’attente de sécurité des applications et des scripts existants ne sera pas interrompue par l’ajout du deuxième paramètre facultatif dans Windows 8 et Windows Server 2012.

Contrairement à la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) , cette méthode effectue les opérations suivantes :

-   Teste si le module de plateforme sécurisée peut déverrouiller le volume, si un protecteur de clé lié au module de plateforme sécurisée existe.
-   Teste si l’ordinateur peut lire un lecteur flash USB qui contient un fichier de clé externe au démarrage, si le volume est déverrouillé par une clé externe (y compris une clé de démarrage).
-   Nécessite un redémarrage de l’ordinateur pour exécuter le test matériel.
-   Commence le chiffrement uniquement si le test matériel est correctement effectué.
-   Ne peut pas être utilisé sur un volume de données, sur un volume partiellement ou entièrement chiffré, ou pour reprendre le chiffrement.

Avant d’exécuter cette méthode, utilisez les méthodes suivantes pour créer les protecteurs de clé associés :

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Après avoir exécuté cette méthode, effectuez les étapes supplémentaires suivantes :

1.  Insérez dans l’ordinateur un lecteur flash USB qui contient un fichier de clé externe. Cette étape s’applique uniquement si le volume a un protecteur de clé de type « clé externe » ou « TPM et clé de démarrage ».
2.  Redémarrez l'ordinateur.

Lors du redémarrage de l’ordinateur, le test matériel s’exécute automatiquement.

Le chiffrement commence si le test matériel est correctement effectué. Sinon, essayez de résoudre les défaillances matérielles. Exécutez [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) après avoir redémarré l’ordinateur pour obtenir les résultats des tests.

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

 

 
