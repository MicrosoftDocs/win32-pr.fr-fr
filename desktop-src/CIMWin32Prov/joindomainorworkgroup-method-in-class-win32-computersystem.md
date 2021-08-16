---
description: Joint un système informatique à un domaine ou à un groupe de travail.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Méthode JoinDomainOrWorkgroup de la classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9faf923cf6c771e95a7dfb4f0b04f896c54d79c6b5548e97850d867057b065b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834646"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Méthode JoinDomainOrWorkgroup de la \_ classe Win32 ComputerSystem

La méthode **JoinDomainOrWorkGroup** joint un système informatique à un domaine ou à un groupe de travail.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Spécifie le domaine ou le groupe de travail à joindre. Ne peut pas être **null**.

</dd> <dt>

*Mot de passe* \[ dans\]
</dt> <dd>

Si le paramètre de *nom d’utilisateur* spécifie un nom de compte, le paramètre *de mot de passe* doit pointer vers le mot de passe à utiliser lors de la connexion au contrôleur de domaine. Dans le cas contraire, ce paramètre doit avoir la **valeur null**.

</dd> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne de caractères constante se terminant par un caractère **null** qui spécifie le nom du compte à utiliser lors de la connexion au contrôleur de domaine. Vous devez spécifier un nom de domaine NetBIOS et un compte d’utilisateur, par exemple, domaine \\ utilisateur. Si ce paramètre a la **valeur null**, les informations de l’appelant sont utilisées.

Vous pouvez également utiliser le nom d’utilisateur principal (UPPED) sous la forme user@domain .

</dd> <dt>

*AccountOU* \[ dans\]
</dt> <dd>

Spécifie le pointeur vers une chaîne de caractères constante se terminant par un caractère **null** qui contient le nom de format [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) de l’unité d’organisation (UO) pour le compte d’ordinateur. Si vous spécifiez ce paramètre, la chaîne doit contenir un chemin d’accès complet, sinon l' *accent* doit être **null**.

Exemple : «OU = testOU ; DC = domaine ; DC = domaine ; DC = com "

</dd> <dt>

*FJoinOptions* \[ dans\]
</dt> <dd>

Jeu d’indicateurs binaires qui définissent les options de jointure.

<dt>



  (0)


</dt> <dd>

Par défaut. Aucune option de jointure.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETsetup \_ JOINDRE un \_ domaine** (0x00000001)


</dt> <dd>

Joint l’ordinateur à un domaine. Si cette valeur n’est pas spécifiée, joint l’ordinateur à un groupe de travail.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETsetup \_ \_Création de compte** (0x00000002)


</dt> <dd>

Crée le compte sur le domaine.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETsetup \_ \_Mise à niveau de Win9x** (0x00000010)


</dt> <dd>

L’opération de jointure se produit dans le cadre d’une mise à niveau.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETsetup \_ Jonction de domaine \_ \_ si \_ jointe** (0x00000020)


</dt> <dd>

Autorise une jointure à un nouveau domaine même si l’ordinateur est déjà joint à un domaine.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETsetup \_ JONCTION \_ non sécurisée** (0x00000040)


</dt> <dd>

Effectue une jonction non sécurisée.

Cette option demande une jonction de domaine à un compte créé au préalable sans authentification avec les informations d’identification de l’utilisateur du domaine. Cette option peut être utilisée conjointement avec l’option de configuration de l' **\_ ordinateur par mot de \_ \_ passe** . Dans ce cas, *Password* est le mot de passe du compte d’ordinateur créé au préalable.

avant Windows Vista avec SP1 et Windows Server 2008, une jonction non sécurisée ne s’est pas authentifiée auprès du contrôleur de domaine. Toutes les communications ont été effectuées à l’aide d’une session null (non authentifiée). à compter de Windows Vista avec SP1 et Windows Server 2008, le nom et le mot de passe du compte d’ordinateur sont utilisés pour l’authentification auprès du contrôleur de domaine.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETsetup \_ ORDINATEUR \_ Pwd \_ passé** (0x00000080)


</dt> <dd>

Indique que le paramètre *de mot de passe* spécifie un mot de passe de compte d’ordinateur local plutôt qu’un mot de passe utilisateur. Cet indicateur n’est valide que pour les jointures non sécurisées, que vous devez indiquer en définissant également l' \_ indicateur de non-sécurisation de la jonction d’installation \_ .

Si vous définissez cet indicateur, une fois l’opération de jointure réussie, le mot de passe de l’ordinateur est défini sur la valeur du *mot* de passe, si cette valeur est un mot de passe d’ordinateur valide.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETsetup \_ AJOURNEr le \_ \_ jeu de noms de principal** de service (0x00000100)


</dt> <dd>

Indique que le nom de principal du service (SPN) et les propriétés DnsHostName de l’objet ordinateur ne doivent pas être mis à jour pour l’instant.

En règle générale, ces propriétés sont mises à jour pendant l’opération de jointure. Au lieu de cela, ces propriétés doivent être mises à jour lors d’un appel ultérieur à la méthode [**Rename**](rename-method-in-class-win32-computersystem.md) . Ces propriétés sont toujours mises à jour lors de l’opération de changement de nom.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETsetup \_ JOINDRE \_ un \_ compte DC** (0x00000200)


</dt> <dd>

Autoriser la jonction de domaine si le compte existant est un contrôleur de domaine.

> [!Note]  
> cet indicateur est pris en charge sur Windows Vista et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETsetup \_ \_Contrôleur de périphérique ambigu** (0x00001000)


</dt> <dd>

Lorsque vous rejoignez le domaine, n’essayez pas de définir le contrôleur de domaine préféré dans le registre.

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETsetup \_ AUCUN \_ \_ cache Netlogon** (0x00002000)


</dt> <dd>

Lorsque vous rejoignez le domaine, ne créez pas le cache Netlogon.

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETsetup \_ Ne pas \_ contrôler les \_ services** (0x00004000)


</dt> <dd>

Lorsque vous rejoignez le domaine, ne forcez pas le démarrage du service Netlogon.

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETsetup \_ DÉFINIR \_ le \_ nom** de l’ordinateur (0x00008000)


</dt> <dd>

Quand vous joignez le domaine pour une jointure hors connexion uniquement, définissez le nom d’hôte de l’ordinateur cible et le nom NetBIOS.

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETsetup \_ FORCER \_ le \_ jeu de SPN** (0x00010000)


</dt> <dd>

Quand vous joignez le domaine, remplacez d’autres paramètres lors de la jonction de domaine et définissez le nom de principal du service (SPN).

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETsetup \_ AUCUNE \_ \_ réutilisation de compte** (0x00020000)


</dt> <dd>

Quand vous joignez le domaine, ne réutilisez pas un compte existant.

> [!Note]  
> cet indicateur est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETsetup \_ IGNORER les \_ \_ indicateurs non pris en charge** (0x10000000)


</dt> <dd>

Si ce bit est défini, les indicateurs non reconnus sont ignorés par la fonction **JoinDomainOrWorkGroup** et [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comporte comme si les indicateurs n’étaient pas définis.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un [code d’erreur système](/windows/desktop/Debug/system-error-codes), qui peut inclure l’une des valeurs numériques suivantes. Tout autre nombre indique une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

L’accès est refusé.

</dd> <dt>

**87**
</dt> <dd>

Le paramètre est incorrect.

</dd> <dt>

**110**
</dt> <dd>

le système ne peut pas ouvrir l’objet spécifié.

</dd> <dt>

**1323**
</dt> <dd>

Impossible de mettre à jour le mot de passe.

</dd> <dt>

**1326**
</dt> <dd>

Échec de l’ouverture de session : nom d’utilisateur inconnu ou mot de passe incorrect.

</dd> <dt>

**1355**
</dt> <dd>

Le domaine spécifié n’existe pas ou n’a pas pu être contacté.

</dd> <dt>

**2224**
</dt> <dd>

Le compte existe déjà.

</dd> <dt>

**2691**
</dt> <dd>

L’ordinateur est déjà joint au domaine.

</dd> <dt>

**2692**
</dt> <dd>

L’ordinateur n’est pas actuellement joint à un domaine.

</dd> <dt>

**\_ \_ connexion chiffrée WBEM \_ \_ requise**
</dt> <dd>

0x80041087

Le *mot de passe* et le *nom d’utilisateur* sont spécifiés, mais le niveau d’authentification n’est pas le niveau d’authentification RPC de la **\_ \_ \_ \_ \_ confidentialité**. pour Visual Basic, **wbemErrEncryptedConnectionRequired** est retourné.

</dd> <dt>

**Autres**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarques

Lors du déplacement d’un ordinateur d’un domaine vers un groupe de travail, vous devez supprimer l’ordinateur du domaine (avec un appel à [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) avant d’appeler cette méthode pour joindre un groupe de travail (avec un appel à **JoinDomainOrWorkGroup**). Après avoir appelé cette méthode, redémarrez l’ordinateur affecté pour appliquer les modifications.

Le *nom d’utilisateur* et le *mot de passe* peuvent être **null**. toutefois, l’authentification de la connexion à WMI doit être 6 dans script ou **WbemAuthenticationLevelPktPrivacy** dans Visual Basic et dans d’autres langues qui peuvent utiliser la bibliothèque [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) . Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

En C++, définissez l’authentification au **niveau de la \_ \_ \_ \_ \_ confidentialité** de l’authentification au niveau de l’authentification RPC C dans [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), pour l’ensemble du processus, ou dans [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), pour une connexion au proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Pour plus d’informations, consultez Définition de l' [authentification à l’aide de C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) et [définition de la sécurité sur IWbemServices et d’autres proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Exemples

L’exemple [rejoindre un ordinateur dans un domaine](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell joint un ordinateur à un domaine.

L’exemple de code VBScript suivant joint un ordinateur à un domaine et crée le compte de l’ordinateur dans Active Directory.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



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

[**Méthode UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

