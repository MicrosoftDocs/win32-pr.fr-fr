---
description: Modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Méthode ChangeOwnerAuth de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004677"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Méthode ChangeOwnerAuth de la \_ classe TPM Win32

La méthode **ChangeOwnerAuth** de la [**classe \_ TPM Win32**](win32-tpm.md) modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldOwnerAuth* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui nomme la valeur d’autorisation du propriétaire du module de plateforme sécurisée (TPM) actuelle de l’appareil. Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir un mot de passe en cette valeur d’autorisation. Le paramètre *OldOwnerAuth* n’est pas fourni ou une chaîne vide est fournie, cette méthode obtient la valeur du Registre si elle est présente.

</dd> <dt>

*NewOwnerAuth* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui nomme la nouvelle valeur d’autorisation du propriétaire du module de plateforme sécurisée. Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir un mot de passe en cette valeur d’autorisation. Le paramètre *NewOwnerAuth* ne peut pas être vide ou avoir la **valeur null.**

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | La méthode a réussi.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | La valeur actuelle de l’autorisation du propriétaire du module de plateforme sécurisée est incorrecte.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente. Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ Le \_ schéma E ad \_ \_ n’est pas \_ installé**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | Impossible d’enregistrer les informations de récupération sur le réseau. L’ordinateur a été configuré pour stocker les informations de récupération à Active Directory Domain Services. Pour obtenir des instructions sur la configuration de Active Directory, consultez [chiffrement de lecteur BitLocker Guide de configuration : sauvegarde des informations de récupération BitLocker et TPM dans Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).<br/> |
| <dl> <dt>**Échec**</dt> <dt>de la connexion 2147943755 (0x8007054B)</dt> </dl>                  | Impossible d’enregistrer les informations de récupération sur le réseau. L’ordinateur a été configuré pour stocker les informations de récupération à Active Directory Domain Services. Une connexion réseau est nécessaire pour continuer.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Remarques

La méthode **ChangeOwnerAuth** sauvegarde la nouvelle autorisation du propriétaire du module de plateforme sécurisée sur Active Directory Domain Services si les paramètres de stratégie de groupe appropriés ont été configurés.

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
</dt> </dl>

 

 
