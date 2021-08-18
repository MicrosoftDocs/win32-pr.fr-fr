---
description: Autorise le propriétaire du module de plateforme sécurisée à activer ou à reprendre le module de plateforme sécurisée.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Activer la méthode de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: ce3103b3845a56a8de8ba4245a2803ef7bcb7624a4781dc658c48ff277354796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004547"
---
# <a name="enable-method-of-the-win32_tpm-class"></a>Activer la méthode de la \_ classe TPM Win32

La méthode **Enable** de la [**classe \_ TPM Win32**](win32-tpm.md) permet au propriétaire du module de plateforme sécurisée d’activer ou de reprendre le module de plateforme sécurisée.

Pour exécuter cette méthode, le module de plateforme sécurisée doit déjà avoir un propriétaire. Pour activer un module de plateforme sécurisée qui n’a pas encore de propriétaire, utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 Enable(
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



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
