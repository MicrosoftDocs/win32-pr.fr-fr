---
description: Supprime un système informatique d’un domaine ou d’un groupe de travail.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Méthode UnjoinDomainOrWorkgroup de la classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861601"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Méthode UnjoinDomainOrWorkgroup de la \_ classe Win32 ComputerSystem

La méthode **UnjoinDomainOrWorkgroup** supprime un système informatique d’un domaine ou d’un groupe de travail.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Mot de passe* \[ dans\]
</dt> <dd>

Si le paramètre de *nom d’utilisateur* spécifie un nom de compte, le paramètre *de mot de passe* doit pointer vers le mot de passe à utiliser lors de la connexion au contrôleur de domaine. Dans le cas contraire, ce paramètre doit avoir la **valeur null**.

> [!Note]  
> Le *mot de passe* doit utiliser un niveau d’authentification élevé, non inférieur à la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC**, lors de la connexion à winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur le pointeur [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . S’il est local à winmgmt, ce n’est pas un problème.

 

</dd> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne de caractères constante se terminant par un caractère null qui spécifie le nom du compte à utiliser lors de la connexion au contrôleur de domaine. Vous devez spécifier un domaine et un compte d’utilisateur, par exemple, « domaine \\ utilisateur » ou « user@domain ». Si ce paramètre a la **valeur null**, le contexte de l’appelant est utilisé.

> [!Note]  
> Le *nom d’utilisateur* doit utiliser un niveau d’authentification élevé, non inférieur à la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC**, lors de la connexion à winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur le pointeur [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . S’il est local à winmgmt, ce n’est pas un problème.

 

</dd> <dt>

*FUnjoinOptions* \[ dans\]
</dt> <dd>

Jeu d’indicateurs binaires définissant les options de jointure.

<dt>



  (0)


</dt> <dd>

Par défaut. Aucune option.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETsetup \_ \_Suppression de compte** (4)


</dt> <dd>

Désactivez le compte de Active Directory après l’opération d’annulation de la jointure, mais ne supprimez pas le compte.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode **UnjoinDomainOrWorkgroup** retourne 0 (zéro) en cas de réussite ou lorsqu’aucune option n’est impliquée. Toute autre valeur indique une erreur. Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Autre** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Notes

Après avoir appelé cette méthode, redémarrez l’ordinateur affecté pour appliquer les modifications.

## <a name="examples"></a>Exemples

[L’ordinateur n’est pas joint à un domaine](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) L’exemple VBScript disjoint l’ordinateur local de son domaine actuel et désactive le compte d’ordinateur.

L’exemple de non- [jointure d’un ordinateur d’un domaine à l’aide d’un script VBS](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) déjoint un ordinateur spécifié d’un domaine. .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ComputerSystem Win32**](win32-computersystem.md)
</dt> <dt>

[**Méthode JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

