---
description: Décrit l’installation locale de WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916955"
---
# <a name="__cimomidentification-class"></a>\_\_CIMOMIdentification, classe

La classe système **\_ \_ CIMOMIdentification** décrit l’installation locale de WMI. Il s’agit d’une classe singleton. Il n’existe qu’une seule instance. La classe **\_ \_ CIMOMIdentification** est disponible uniquement dans les espaces de noms **root** et **root \\ par défaut** . Les utilisateurs interrogent l’instance pour obtenir des informations sur l’installation de WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ CIMOMIdentification** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ CIMOMIdentification** possède les propriétés suivantes.

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de l’installation. Cette propriété est vide après l’installation du système d’exploitation pour la première fois.

Si le référentiel WMI a été supprimé, puis recréé, cette propriété contient la date et l’heure de la création du dépôt.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la version de l’image réelle contenant le service WMI qui a créé le référentiel Common Information Model (CIM). Étant donné que le format de référentiel peut changer d’une version à l’autre de WMI, cette propriété autorise les futures mises à niveau de WMI pour déterminer si la base de données doit être mise à niveau. Le format est le suivant :

"1.00.183.0000"

où le premier chiffre est la version principale, les deux chiffres suivants sont des versions mineures, et les trois chiffres suivants sont le numéro de Build. Les chiffres restants ne sont pas utilisés.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la version de l’image réelle contenant le service WMI qui a créé le référentiel CIM. Étant donné que le format de référentiel peut changer d’une version à l’autre de WMI, cette propriété autorise les futures mises à niveau de WMI pour déterminer si la base de données doit être mise à niveau. Le format est le suivant :

"1.00.183.0000"

où le premier chiffre est la version principale, les deux chiffres suivants sont des versions mineures, et les trois chiffres suivants sont le numéro de Build. Les chiffres restants ne sont pas utilisés.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Répertoire d’installation.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ CIMOMIdentification** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.

## <a name="examples"></a>Exemples

l’exemple de code VBScript suivant décrit comment afficher les informations d’identification du modèle d’objet CIM et provient de l’exemple de répertoire situé dans \\ \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ sysmgmt \\ wmi \\ scripting.


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



l’exemple de code Perl suivant décrit comment afficher les informations d’identification du modèle d’objet CIM et provient de l’exemple de répertoire situé dans \\ \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ sysmgmt \\ wmi \\ scripting.


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Root<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

