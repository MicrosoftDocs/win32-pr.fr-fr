---
description: Lance le partage pour une ressource de serveur.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 582e255223b6eb971fd447c7884ff730662a1b344c107791b1a57a074c2c1354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504769"
---
# <a name="create-method-of-the-win32_share-class"></a>Créer une méthode de la \_ classe de partage Win32

La méthode **Create**   [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) lance le partage pour une ressource de serveur.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

chemin d’accès Local du partage de Windows.

Par exemple, « C : \\ Program Files ».

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Transmet l’alias à un chemin d’accès configuré en tant que partage sur un système d’ordinateur exécutant Windows.

Exemple : « public ».

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Passe le type de ressource partagé. Les types incluent des lecteurs de disque, des files d’attente à l’impression, des communications interprocessus (IPC) et des périphériques généraux. Il peut s’agir de l’une des valeurs suivantes.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Lecteur de disque** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**File d’attente** à l’impression (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Appareil** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Administrateur de lecteur de disque** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrateur de file d’attente** à l’impression (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrateur d’appareil** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Administrateur IPC** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ dans, facultatif\]
</dt> <dd>

Limite du nombre maximal d’utilisateurs autorisés à utiliser simultanément cette ressource.

Exemple : 10. Ce paramètre est facultatif.

</dd> <dt>

*Description* \[ dans, facultatif\]
</dt> <dd>

Commentaire facultatif pour décrire la ressource partagée. Ce paramètre est facultatif.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

Mot de passe (lorsque le serveur s’exécute avec la sécurité au niveau du partage) pour la ressource partagée. Si le serveur s’exécute avec la sécurité au niveau de l’utilisateur, ce paramètre est ignoré. Ce paramètre est facultatif.

</dd> <dt>

*Accès* \[ dans, facultatif\]
</dt> <dd>

Descripteur de sécurité pour les autorisations au niveau de l’utilisateur. Un descripteur de sécurité contient des informations sur les autorisations, le propriétaire et les capacités d’accès de la ressource. Si ce paramètre n’est pas fourni ou a la **valeur null**, tout le monde dispose d’un accès en lecture au partage. Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) et [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Nom non valide** (9)
</dt> <dt>

**Niveau non valide** (10)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Partage en double** (22)
</dt> <dt>

**Chemin d’accès Redirigé** (23)
</dt> <dt>

**Périphérique ou répertoire inconnu** (24)
</dt> <dt>

**Nom de réseau introuvable** (25)
</dt> <dt>

**Autre** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarques

**Create** est une méthode statique.

Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter la **création**. L’opérateur Print peut uniquement ajouter des files d’attente d’impression. L’opérateur de communication peut uniquement ajouter des files d’attente d’appareils de communication.

## <a name="examples"></a>Exemples

L’exemple d' [exportation et d’importation partages](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell exporte et importe des partages de fichiers et définit des autorisations de partage. De même, l’exemple [créer un partage et définir des autorisations](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) crée également un nouveau partage et définit les autorisations de partage.

Le code PowerShell suivant crée un partage.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



L’exemple de code précédent retourne ce qui suit :

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

L' \# exemple de code C suivant décrit comment appeler la méthode Create.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
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

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Partage Win32**](win32-share.md)
</dt> </dl>

 

