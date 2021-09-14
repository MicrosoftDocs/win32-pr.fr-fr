---
description: représente un travail d’impression généré par une application Windows. toute unité de travail générée par la commande d’impression d’une application exécutée sur un ordinateur qui exécute sur un système d’exploitation Windows est un descendant ou un membre de cette classe.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124256"
---
# <a name="win32_printjob-class"></a>\_Classe PrintJob Win32

la [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrintJob Win32** représente un travail d’impression généré par une application Windows. toute unité de travail générée par la commande d’impression d’une application exécutée sur un ordinateur qui exécute sur un système d’exploitation Windows est un descendant ou un membre de cette classe.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>Membres

La **classe \_ PrintJob Win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ PrintJob Win32** possède ces méthodes.



| Méthode                                                  | Description                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Suspendre**](pause-method-in-class-win32-printjob.md)   | Suspend un travail d’impression.<br/>    |
| [**Sort**](resume-method-in-class-win32-printjob.md) | Poursuit un travail d’impression.<br/> |



 

### <a name="properties"></a>Propriétés

La **classe \_ PrintJob Win32** possède ces propriétés.

<dl> <dt>

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

**Couleur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne qui indique si le document est imprimé en couleur ou monochrome. Certaines imprimantes couleur ont la possibilité d’imprimer à l’aide d’un vrai noir au lieu d’une combinaison jaune, cyan et magenta. True black crée généralement un texte plus sombre et plus clair pour les documents. Cette option est utile uniquement pour les imprimantes couleur qui prennent en charge l’impression noir.

Les valeurs sont :

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**Colorimétrique**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**Monochrome**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Format des données pour ce travail d’impression. cela indique au pilote d’imprimante de convertir les données (texte générique, PostScript ou PCL) avant l’impression, ou d’imprimer dans un format brut (pour les graphiques et les images).

Exemple : « texte »

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

**Document**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du travail d’impression. L’utilisateur voit ce nom lors de l’affichage des documents en attente d’impression.

exemple : « Microsoft Word-Review.doc »

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du pilote d’imprimante utilisé pour le travail d’impression.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée d’exécution du travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**HostPrintQueue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur sur lequel le travail d’impression est créé.

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

**JobId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro d’identification du travail. Il est utilisé par d’autres méthodes en tant que handle d’un travail mis en attente sur l’imprimante.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui représente l’état du travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Étiquette par laquelle l’objet est connu. Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’utilisateur est averti en cas d’achèvement ou d’échec de la tâche.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**Propriétaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Utilisateur qui a envoyé le travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**PagesPrinted**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pages imprimées. Cette valeur peut être 0 (zéro) si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre).
</dt> </dl>

Longueur du papier.

Exemple : 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille du papier utilisé pour imprimer le travail. La valeur est l’une des tailles de papier possibles pour l’imprimante spécifiée dans la propriété **PaperSizesSupported** de la classe [**Win32 \_ Printer**](win32-printer.md) .

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre).
</dt> </dl>

Largeur du papier.

Exemple : 2159

</dd> <dt>

**Paramètres**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètres facultatifs à envoyer au processeur d’impression. Pour plus d’informations, consultez la propriété **PrintProcessor** .

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Service du processeur d’impression utilisé pour traiter le travail d’impression. Un processeur d’imprimante fonctionne conjointement avec le pilote d’imprimante pour fournir une traduction supplémentaire des données de l’imprimante pour l’imprimante et peut également être utilisé pour fournir des options spéciales, telles qu’une page de titre pour le travail.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Importance de l’exécution d’un travail.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**Taille**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (octets)
</dt> </dl>

Taille du travail d’impression.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de début de la tâche.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

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

**StatusMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bitmap des États possibles liés à ce travail d’impression.

<dt>

1 (0x1)
</dt> <dd>

Suspendu

</dd> <dt>

2 (0X2)
</dt> <dd>

Erreur

</dd> <dt>

4 (0x4)
</dt> <dd>

Suppression

</dd> <dt>

8 (0x8)
</dt> <dd>

Attente

</dd> <dt>

16 (0x10)
</dt> <dd>

Impression

</dd> <dt>

32 (0x20)
</dt> <dd>

Hors connexion

</dd> <dt>

64 (0x40)
</dt> <dd>

Paperout

</dd> <dt>

128 (0x80)
</dt> <dd>

Affiche

</dd> <dt>

256 (0x100)
</dt> <dd>

Deleted

</dd> <dt>

512 (0x200)
</dt> <dd>

\_DevQ bloqué

</dd> <dt>

1024 (0x400)
</dt> <dd>

\_Demande d’intervention de l’utilisateur \_

</dd> <dt>

2048 (0x800)
</dt> <dd>

Redémarrer

</dd> </dl>

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail a été soumis.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pages nécessaires pour terminer le travail. Cette valeur peut être 0 (zéro) si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle le travail n’est pas valide ou doit être arrêté.

Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La **classe \_ PrintJob Win32** est dérivée de la [**\_ tâche CIM**](cim-job.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant décrit comment récupérer des statistiques de travaux d’impression à partir d’instances de **Win32 \_ PrintJob**.


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



L’exemple de code perl suivant décrit comment récupérer des statistiques de travaux d’impression à partir d’instances de **Win32 \_ PrintJob**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Travail CIM**](./cim-job.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
