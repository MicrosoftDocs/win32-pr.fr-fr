---
description: Réinitialise le module de plateforme sécurisée à son état d’usine par défaut.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Méthode Clear de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209674"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Méthode Clear de la \_ classe TPM Win32

La méthode **Clear** de la [**classe \_ TPM Win32**](win32-tpm.md) réinitialise le module de plateforme sécurisée (TPM) à son état d’usine par défaut. Un propriétaire du module de plateforme sécurisée peut utiliser cette méthode pour annuler la propriété du module de plateforme sécurisée et invalider les matériaux de chiffrement créés par le propriétaire précédent. Cette méthode suspend BitLocker si l’appel de peut entraîner la nécessité d’une récupération BitLocker. BitLocker reprendra automatiquement une fois que le module de plateforme sécurisée a été approvisionné.

> [!Caution]  
> En effaçant le module de plateforme sécurisée, vous perdez toutes les clés TPM créées et utilisées par les applications. Si ces clés ont été utilisées pour chiffrer les données, assurez-vous de disposer d’une autre méthode pour accéder aux données avant d’effacer le module de plateforme sécurisée.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Origine* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie le propriétaire du module de plateforme sécurisée. Cette chaîne doit être une chaîne encodée en base64 contenant exactement 20 octets de données binaires. Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu. Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                         | Description                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | La méthode a réussi.<br/>                                                                                                                                                |
| <dl> <dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | La valeur d’autorisation du propriétaire fournie ne peut pas effectuer la requête.<br/>                                                                                                        |
| <dl> <dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente. Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Notes

L’exécution de cette méthode peut aider à préparer un ordinateur équipé d’un module de plateforme sécurisée pour le recyclage.

Pour effacer le module de plateforme sécurisée mais n’avoir plus l’autorisation de propriétaire du module de plateforme sécurisée, vous devez disposer d’un accès physique à l’ordinateur. La méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) comprend des fonctionnalités permettant d’effacer le module de plateforme sécurisée sans l’autorisation du propriétaire du module de plateforme sécurisée.

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

 

 
