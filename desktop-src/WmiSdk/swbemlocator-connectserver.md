---
description: Établit une connexion à l’espace de noms sur l’ordinateur spécifié dans le paramètre strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Méthode SWbemLocator. ConnectServer (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541994"
---
# <a name="swbemlocatorconnectserver-method"></a>Méthode SWbemLocator. ConnectServer

La méthode **ConnectServer** de l’objet [**SWbemLocator**](swbemlocator.md) se connecte à l’espace de noms sur l’ordinateur spécifié dans le paramètre *strServer* . L’ordinateur cible peut être local ou distant, mais WMI doit être installé. Pour obtenir des exemples et une comparaison avec le type de moniker Connection, consultez [création d’un script WMI](creating-a-wmi-script.md).

À compter de Windows Vista, **SWbemLocator. ConnectServer** peut se connecter avec des ordinateurs exécutant IPv6 à l’aide d’une adresse IPv6 dans le paramètre *strServer* . Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strServer* \[ dans, facultatif\]
</dt> <dd>

Nom de l’ordinateur auquel vous vous connectez. Si l’ordinateur distant se trouve dans un domaine différent du compte d’utilisateur sous lequel vous vous connectez, utilisez le nom d’ordinateur complet. Si vous ne fournissez pas ce paramètre, l’appel est défini par défaut sur l’ordinateur local.

Exemple : `server1.network.fabrikam`

Vous pouvez également utiliser une adresse IP dans ce paramètre. Si l’adresse IP est au format IPv6, l’ordinateur cible doit exécuter IPv6. Une adresse IPv4 ressemble à ceci `123.123.123.123`

Une adresse IP au format IPv6 ressemble à ce qui suit. `2010:836B:4179::836B:4179`

Pour plus d’informations sur DNS et IPv4, consultez la section Notes.

</dd> <dt>

*strNameSpace* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui spécifie l’espace de noms auquel vous vous connectez. Par exemple, pour vous connecter à l' \\ espace de noms racine par défaut, utilisez la racine \\ par défaut. Si vous ne spécifiez pas ce paramètre, la valeur par défaut est l’espace de noms configuré comme espace de noms par défaut pour les scripts. Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).

Exemple : « root \\ cimv2 »

</dd> <dt>

*strUser* \[ dans, facultatif\]
</dt> <dd>

Nom d’utilisateur à utiliser pour se connecter. La chaîne peut être sous la forme d’un nom d’utilisateur ou d’un nom d’utilisateur de domaine \\ . Laissez ce paramètre vide pour utiliser le contexte de sécurité actuel. Le paramètre *strUser* doit être utilisé uniquement avec les connexions aux serveurs WMI distants. Si vous tentez de spécifier *strUser* pour une connexion WMI locale, la tentative de connexion échoue. Si l’authentification Kerberos est utilisée, le nom d’utilisateur et le mot de passe spécifiés dans *strUser* et *strPassword* ne peuvent pas être interceptés sur un réseau. Vous pouvez utiliser le format UPN pour spécifier le *strUser*.

Exemple : « nom_domaine \\ nom_utilisateur »

> [!Note]  
> Si un domaine est spécifié dans *strAuthority*, le domaine ne doit pas être spécifié ici. La spécification du domaine dans les deux paramètres génère une erreur de paramètre non valide.

 

</dd> <dt>

*strPassword* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui spécifie le mot de passe à utiliser lors de la tentative de connexion. Laissez le paramètre vide pour utiliser le contexte de sécurité actuel. Le paramètre *strPassword* doit être utilisé uniquement avec les connexions aux serveurs WMI distants. Si vous tentez de spécifier *strPassword* pour une connexion WMI locale, la tentative de connexion échoue. Si l’authentification Kerberos est en cours d’utilisation, le nom d’utilisateur et le mot de passe spécifiés dans *strUser* et *strPassword* ne peuvent pas être interceptés sur le réseau.

</dd> <dt>

*strLocale* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui spécifie le code de localisation. Si vous souhaitez utiliser les paramètres régionaux actuels, laissez-le vide. Si la valeur n’est pas vide, ce paramètre doit être une chaîne qui indique les paramètres régionaux souhaités où les informations doivent être récupérées. Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS \_ xxxx », où xxxx est une chaîne au format hexadécimal qui indique le LCID. Par exemple, l’anglais américain s’affiche sous la forme « MS \_ 409 ».

</dd> <dt>

*strAuthority* \[ dans, facultatif\]
</dt> <dd>

<dt>

""
</dt> <dd>

Ce paramètre est facultatif. Toutefois, si elle est spécifiée, seuls Kerberos ou NTLMDomain peuvent être utilisés.

</dd> <dt>

Clé
</dt> <dd>

Si le paramètre *strAuthority* commence par la chaîne « Kerberos : », l’authentification Kerberos est utilisée et ce paramètre doit contenir un nom de principal Kerberos. Le nom principal Kerberos est spécifié sous la forme Kerberos :*Domain*, par exemple `Kerberos:fabrikam` où `fabrikam` est le serveur auquel vous tentez de vous connecter.

Exemple : « Kerberos : domaine »

</dd> <dt>

NTLMDomain
</dt> <dd>

Pour utiliser l’authentification NTLM (NT LAN Manager), vous devez la spécifier sous la forme NTLMDomain :*Domain*, par exemple `NTLMDomain:fabrikam` où `fabrikam` est le nom du domaine.

Exemple : « NTLMDomain : DOMAIN »

</dd> </dl>

Si vous laissez ce paramètre vide, le système d’exploitation négocie avec COM pour déterminer si l’authentification NTLM ou Kerberos est utilisée. Ce paramètre ne doit être utilisé qu’avec des connexions à des serveurs WMI distants. Si vous tentez de définir l’autorité pour une connexion WMI locale, la tentative de connexion échoue.

> [!Note]  
> Si le domaine est spécifié dans *strUser*, qui est l’emplacement par défaut, il ne doit pas être spécifié ici. La spécification du domaine dans les deux paramètres génère une erreur de paramètre non valide.

 

</dd> <dt>

*iSecurityFlags* \[ dans, facultatif\]
</dt> <dd>

Utilisé pour passer des valeurs d’indicateur à **ConnectServer**.

<dt>

0 (0x0)
</dt> <dd>

La valeur 0 pour ce paramètre entraîne le retour de l’appel à **ConnectServer** uniquement après l’établissement de la connexion au serveur. Cela peut empêcher votre programme de répondre indéfiniment si la connexion ne peut pas être établie.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait * * * * (128 (0x80))


</dt> <dd>

Le retour de l’appel **ConnectServer** est garanti à 2 minutes ou moins. Utilisez cet indicateur pour empêcher votre programme de cesser de répondre indéfiniment si la connexion ne peut pas être établie.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, WMI retourne un objet [**SWbemServices**](swbemservices.md) qui est lié à l’espace de noms spécifié dans *strNameSpace* sur l’ordinateur spécifié dans *strServer*.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **ConnectServer** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Le nom d’utilisateur et le mot de passe actuels ou spécifiés ne sont pas valides ou ne sont pas autorisés à établir la connexion.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100E)
</dt> <dd>

L’espace de noms spécifié n’existait pas sur le serveur.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

Une erreur réseau s’est produite, empêchant le fonctionnement normal.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **ConnectServer** est souvent utilisée lors de la connexion à un compte avec des informations d’identification de nom d’utilisateur et de mot de passe différentes sur un ordinateur distant, car vous ne pouvez pas spécifier un mot de passe différent dans une chaîne de [moniker](constructing-a-moniker-string.md) . Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

L’utilisation d’une adresse IPv4 pour se connecter à un serveur distant peut entraîner un comportement inattendu. La cause la plus probable est l’obsolescence des entrées DNS dans votre environnement. Dans ces circonstances, l’entrée PTR périmée pour l’ordinateur est utilisée, avec des résultats imprévisibles. Pour éviter ce comportement, vous pouvez ajouter un point (".") à l’adresse IP avant d’appeler ConnectServer. Cela provoque l’échec de la recherche DNS inversée, mais peut permettre à l’appel **ConnectServer** de réussir sur l’ordinateur approprié.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant décrit comment se connecter à un ordinateur distant pour obtenir des données [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) . Le nom de domaine spécifié dans *strDomain* est utilisé dans *strAuthority*.


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



L’extrait de code PowerShell suivant accède à un serveur distant et répertorie les classes WMI disponibles.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**M**](swbemservices.md)
</dt> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Création d’un script WMI](creating-a-wmi-script.md)
</dt> </dl>

 

