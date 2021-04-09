---
description: La \_ classe de partage Win32 représente une ressource partagée sur un système informatique exécutant Windows. Il peut s’agir d’un lecteur de disque, d’une imprimante, d’une communication entre processus ou d’un autre appareil partageable. Pour plus d’informations sur la récupération des classes WMI, consultez récupération d’une classe.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111203"
---
# <a name="win32_share-class"></a>\_Classe de partage Win32

La classe de **\_ partage Win32** représente une ressource partagée sur un système informatique exécutant Windows. Il peut s’agir d’un lecteur de disque, d’une imprimante, d’une communication entre processus ou d’un autre appareil partageable. Pour plus d’informations sur la récupération des classes WMI, consultez [récupération d’une classe](../wmisdk/retrieving-a-class.md).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a>Membres

La classe de **\_ partage Win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ partage Win32** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créés**](create-method-in-class-win32-share.md)               | Méthode de classe qui initie le partage pour une ressource de serveur.<br/>                                                                                                                                               |
| [**Supprimer**](delete-method-in-class-win32-share.md)               | Méthode de classe qui supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.<br/>                                                                       |
| [**GetAccessMask**](getaccessmask-method-in-class-win32-share.md) | Retourne les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée. Vous devez utiliser cette méthode à la place de la propriété **AccessMask** , qui est toujours **null**.<br/> |
| [**SetShareInfo**](setshareinfo-method-in-class-win32-share.md)   | Méthode de classe qui définit les paramètres d’une ressource partagée.<br/>                                                                                                                                              |



 

### <a name="properties"></a>Propriétés

La classe de **\_ partage Win32** possède ces propriétés.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété est obsolète et n’est plus utilisée. Utilisez la méthode [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) à la place. La valeur de la propriété **AccessMask** est définie sur **null** par WMI. Pour plus d’informations sur la définition de l’accès lors de la création d’un partage, consultez la méthode [**Create**](create-method-in-class-win32-share.md) .

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")
</dt> </dl>

Le nombre d’utilisateurs simultanés pour cette ressource a été limité. Si la valeur est **true**, la valeur de la propriété **MaximumAllowed** est ignorée.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Brève description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")
</dt> </dl>

Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément. La valeur est valide uniquement si la propriété **AllowMaximum** est définie sur **false**.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api partagent les \| [**\_ informations \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")
</dt> </dl>

Alias donné à un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.

Windows 2008 exemple : « \\ SERVEUR01 \\ public »-windows Server 2008 nécessite que vous détrouviez l’UNC dans le nom.

</dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Chemin d’accès local du partage Windows.

Exemple : « C : \\ Program Files »

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Chaîne qui indique l’état actuel de l’objet. L’état opérationnel et non opérationnel peut être défini. L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ». « Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).

L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ». Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")
</dt> </dl>

Type de ressource partagée. Les types sont les suivants : lecteurs de disque, files d’attente à l’impression, communications interprocessus (IPC) et périphériques généraux.

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


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ partage Win32** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).

La méthode Create de cette classe est une méthode statique. Les méthodes **Delete**, **GetAccessMask** et **SetShareInfo** sont toutes des méthodes d’instance.

Selon vos autorisations de sécurité, vous risquez de ne pas pouvoir récupérer toutes les propriétés de cette classe. Par exemple, les propriétés **AllowMaximum**, **MaximumAllowed**, **path** et **type** peuvent retourner la valeur null. En règle générale, les utilisateurs avec pouvoir et les administrateurs peuvent récupérer toutes les valeurs de propriété.

## <a name="examples"></a>Exemples

L'[exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) du centre de scripts suivant répertorie tous les partages sur un ordinateur et répertorie toutes les autorisations de partage pour chaque partage.

Les [informations de partage obtenir des informations similaires à celles de Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample interrogent \_ le partage Win32 et fournissent les résultats.

L’exemple PowerShell suivant affiche les partages sur le système local.


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



Sinon, si vous souhaitez filtrer plus précisément, vous pouvez utiliser l’extrait de code PowerShell suivant :


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



L’exemple VBScript suivant affiche les partages sur le système local.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[Tâches WMI : fichiers et dossiers](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
