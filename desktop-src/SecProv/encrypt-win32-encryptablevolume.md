---
description: Commence le chiffrement d’un volume entièrement déchiffré, ou reprend le chiffrement d’un volume partiellement chiffré.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Méthode Encrypt de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035204"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Méthode Encrypt de la \_ classe EncryptableVolume Win32

La méthode **Encrypt** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) commence le chiffrement d’un volume entièrement déchiffré, ou reprend le chiffrement d’un volume partiellement chiffré. Lorsque le chiffrement est suspendu ou en cours, cette méthode se comporte comme [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Lorsque le déchiffrement est suspendu ou en cours, cette méthode arrête le déchiffrement et commence le chiffrement.

> [!Note]  
> Si le lecteur est chiffré sur le matériel, cette méthode ne chiffre pas les données. Au lieu de cela, il définit l’état de la bande sur « déverrouillé » à « toujours déverrouillé ». Si la bande est verrouillée, déverrouillée ou est en lecture seule, le lecteur est considéré comme étant chiffré.

 

**Windows Vista :** Le chiffrement d’un volume autre que le volume du système d’exploitation en cours d’exécution n’est pas pris en charge.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncryptionMethod* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Entier non signé qui spécifie l’algorithme de chiffrement et la taille de clé utilisés pour chiffrer le volume. Si ce paramètre est supérieur à zéro et que le volume est partiellement ou entièrement chiffré, *EncryptionMethod* doit correspondre à la méthode de chiffrement existante du volume. Si ce paramètre est supérieur à zéro et que le paramètre de stratégie de groupe correspondant est activé avec une valeur valide, *EncryptionMethod* doit correspondre au paramètre stratégie de groupe.

Pour obtenir la liste des valeurs de EncryptionMethod possibles, consultez la méthode [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .

La valeur par défaut pour Windows 7 ou une valeur inférieure est : 1 (AES \_ 128 \_ avec \_ diffuseur).

La valeur par défaut pour Windows 8, Windows 8.1 ou Windows 10, version 1507 est : 3 (AES \_ 128).

La valeur par défaut pour Windows 10, version 1511 ou ultérieure est : 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ dans, facultatif\]
</dt> <dd>

Type : **UInt32**

Indicateurs qui décrivent le comportement de chiffrement.

**Windows 7, Windows server 2008 R2, Windows Vista entreprise et Windows server 2008 :** Ce paramètre n’est pas disponible.

Combinaison de 32 bits avec les bits suivants actuellement définis.



| Valeur                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement. Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode **Encrypt** reprend efficacement la conversion et la valeur de ce bit est ignorée. Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu. Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Effectuez une réinitialisation à la demande de l’espace libre du volume. L’appel de la méthode **Encrypt** avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Effectuez l’opération demandée de façon synchrone. L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue. Cet indicateur est pris en charge uniquement avec la méthode **Encrypt** . Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours. Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.

Cette méthode est retournée immédiatement. Si le volume est déjà entièrement chiffré et qu’aucune autre erreur n’est renvoyée, cette méthode retourne 0.



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
<td>Il n’existe aucune clé de chiffrement pour le volume. Désactivez les protecteurs de clé à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista :</strong> Lorsqu’il n’existe aucune clé de chiffrement pour le volume, ERROR_INVALID_OPERATION est retourné à la place. La valeur décimale est 4317 et la valeur hexadécimale est 0x10DD.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </dl></td>
<td>La méthode de chiffrement fournie ne correspond pas à celle du volume partiellement ou entièrement chiffré. Pour continuer le chiffrement, laissez le paramètre <em>EncryptionMethod</em> vide ou utilisez une valeur égale à zéro.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Le volume ne peut pas être chiffré car cet ordinateur est configuré pour faire partie d’un cluster de serveurs.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>Le volume est verrouillé.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Aucun protecteur de clé du type de &quot; mot de passe numérique &quot; n’est spécifié. Le stratégie de groupe nécessite une sauvegarde des informations de récupération pour Active Directory Domain Services. Pour ajouter au moins un protecteur de clé de ce type, utilisez la méthode <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Lorsque vous utilisez cette méthode sans le second paramètre facultatif (selon la définition de Windows 7 et de Windows Vista Enterprise), la méthode lance toujours la conversion en mode complet afin de conserver un comportement à compatibilité descendante. De cette façon, l’attente de sécurité des applications et des scripts existants ne sera pas interrompue par l’ajout du deuxième paramètre facultatif dans Windows 8 et Windows Server 2012.

Vous pouvez appeler [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) pour déterminer si le chiffrement est en cours et le pourcentage du volume qui a été chiffré.

Une fois que le volume est entièrement chiffré et que des protecteurs de clés ont été ajoutés et activés, l’état de protection du volume passe à « activé ».

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

 

 
