---
description: Représente une connexion réseau active dans un environnement Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Classe Win32_NetworkConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748909"
---
# <a name="win32_networkconnection-class"></a>\_Classe NetworkConnection Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection** WMI représente une connexion réseau active dans un environnement Windows.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ NetworkConnection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ NetworkConnection** a ces propriétés.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Liste des droits d’accès au fichier ou répertoire donné détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée. Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)


</dt> <dd>

Accorde le droit de lire des données à partir du fichier. Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)


</dt> <dd>

Accorde le droit d’écrire des données dans le fichier. Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Fichier \_ Ajouter des \_ données (fichier) ou \_ un \_ sous-répertoire d’ajout de fichier** (4)


</dt> <dd>

Accorde le droit d’ajouter des données au fichier. Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)


</dt> <dd>

Accorde le droit de lire les attributs étendus.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)


</dt> <dd>

Accorde le droit d’écrire des attributs étendus.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)


</dt> <dd>

Accorde le droit d’exécuter un fichier. Pour un répertoire, le répertoire peut être parcouru.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)


</dt> <dd>

Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)


</dt> <dd>

Accorde le droit de lire les attributs du fichier.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)


</dt> <dd>

Accorde le droit de modifier les attributs de fichier.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)


</dt> <dd>

Octroie l’accès en suppression.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)


</dt> <dd>

Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)


</dt> <dd>

Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)


</dt> <dd>

Affecte le propriétaire de l’écriture.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)


</dt> <dd>

Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.

</dd> </dl>

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

**Commentaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")
</dt> </dl>

Commentaire fourni par le fournisseur réseau.

</dd> <dt>

**ConnectionState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures de gestion de réseau \| [**utilisent \_ info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **Ui1 \_ Status**")
</dt> </dl>

État actuel de la connexion réseau.

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

**Connecté** (« connecté »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Suspendu** (« suspendu »)


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

**Déconnecté** (« déconnecté »)


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

**Connexion** (« connexion »)


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

**Reconnexion** (« reconnexion »)


</dt> <dd></dd> </dl>

</dd> <dt>

**ConnectionType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")
</dt> </dl>

Type de persistance de la connexion utilisée pour la connexion au réseau.

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

**Connexion active** (« connexion en cours »)


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

**Connexion permanente** (« connexion persistante »)


</dt> <dd></dd> </dl>

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

**DisplayType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")
</dt> </dl>

L’objet réseau doit s’afficher dans une interface utilisateur de navigation réseau.

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

**Domaine** (« domaine »)


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

**Générique** (« Générique »)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Serveur** (« serveur »)


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

**Partage** (« partage »)


</dt> <dd></dd> </dl>

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

**LocalName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")
</dt> </dl>

Nom local du périphérique réseau connecté.

Exemple : "c : \\ public"

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("nom"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures réseau Windows win32api \| [](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")
</dt> </dl>

Nom de la connexion réseau actuelle. Il s’agit de la combinaison des valeurs dans **nom_distant** et **LocalName**.

Exemple : « \\ \\ NTRELEASE (c : \\ public) »

</dd> <dt>

**Persistent**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Windows Networking Functions \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)»)
</dt> </dl>

La connexion sera reconnectée automatiquement par le système d’exploitation lors de la prochaine ouverture de session.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")
</dt> </dl>

Nom du fournisseur propriétaire de la ressource. Cette propriété peut avoir la **valeur null** si le nom du fournisseur est inconnu.

</dd> <dt>

**RemoteName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Nom de ressource réseau distant pour une ressource réseau. Pour une connexion active ou persistante, **nom_distant** contient le nom réseau associé au nom de la valeur dans la propriété **LocalName** . Le nom dans **nom_distant** doit respecter les conventions d’affectation de noms du fournisseur réseau.

Exemple : « \\ \\ NTRELEASE »

</dd> <dt>

**RemovePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Chemin d’accès complet à la ressource réseau.

Exemple : « \\ \\ infosrv1 \\ public »

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")
</dt> </dl>

Type de ressource à énumérer ou à laquelle se connecter.

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

**Disque** (« Disk »)


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

**Imprimer** (« imprimer »)


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

**Any** (« any »)


</dt> <dd></dd> </dl>

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

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Windows Networking Functions \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)»)
</dt> </dl>

Nom d’utilisateur ou nom d’utilisateur par défaut utilisé pour établir une connexion réseau.

Exemple : « système »

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ NetworkConnection** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant récupère des informations sur la connexion au réseau local.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
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
</dt> </dl>

 

 
