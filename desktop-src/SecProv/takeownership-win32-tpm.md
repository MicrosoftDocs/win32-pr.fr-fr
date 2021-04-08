---
description: Installe un propriétaire pour le module de plateforme sécurisée.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Méthode TakeOwnership de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035160"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Méthode TakeOwnership de la \_ classe TPM Win32

La méthode **TakeOwnership** de la [**classe \_ TPM Win32**](win32-tpm.md) installe un propriétaire pour le module de plateforme sécurisée. Le propriétaire du module de plateforme sécurisée peut tirer pleinement parti des fonctionnalités du module TPM. Une fois qu’un propriétaire est défini, aucun autre utilisateur ou logiciel ne peut réclamer la propriété du module de plateforme sécurisée.

Les méthodes [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)et [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) doivent toutes avoir la valeur true pour que la méthode **TakeOwnership** puisse fonctionner correctement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Origine* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie le propriétaire du module de plateforme sécurisée. Cette chaîne doit être une chaîne codée en base64 qui se termine par un caractère null qui contient exactement 20 octets de données binaires. Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu. Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                         | Description                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | La méthode a réussi.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Le paramètre *origine* n’est pas valide.<br/>                                                                                                                                                                 |
| <dl> <dt>**Module TPM \_ \_ \_ Jeu de propriétaires E**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | Un propriétaire existe déjà sur le module de plateforme sécurisée.<br/>                                                                                                                                                                     |
| <dl> <dt>**Module TPM \_ E \_ non \_ endossement**</dt> <dt>2150105123 (0x80280023)</dt> </dl>       | Aucune clé de type EK ne peut être trouvée sur le module de plateforme sécurisée.<br/> Pour créer une paire de clés de type EK sur le module de plateforme sécurisée, consultez la méthode [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .<br/>             |
| <dl> <dt>**Module TPM \_ E \_ installation \_ désactivée**</dt> <dt>2150105099 (0x8028000B)</dt> </dl>     | Un propriétaire ne peut pas être installé sur ce module de plateforme sécurisée.<br/> Pour plus d’informations sur la façon d’autoriser l’installation d’un propriétaire d’appareil, consultez [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente. Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                               |



 

## <a name="remarks"></a>Notes

Les méthodes [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)et [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) doivent toutes avoir la valeur true pour que **TakeOwnership** puisse s’effectuer correctement.

Vous devez utiliser la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour remplacer une phrase secrète par la valeur d’entrée utilisée pour le paramètre *origine* .

La méthode **TakeOwnership** sauvegarde la valeur d’autorisation du propriétaire sur Active Directory si les paramètres de stratégie de groupe appropriés ont été configurés.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
