---
description: Représente les paramètres d’un composant COM (Component Object Model).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515790"
---
# <a name="win32_classiccomclasssetting-class"></a>\_Classe ClassicCOMClassSetting Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ClassicCOMClassSetting** représente les paramètres d’un composant COM (Component Object Model).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ClassicCOMClassSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ClassicCOMClassSetting** a ces propriétés.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

Identificateur global unique (GUID) de l’application COM utilisant ce composant COM.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ default \] ")
</dt> </dl>

GUID de la classe COM vers laquelle ce composant COM sera automatiquement converti.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autotraitéas \[ par défaut \] ")
</dt> </dl>

GUID du composant COM qui émulera automatiquement les instances de cette classe.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machines \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ par défaut \] ")
</dt> </dl>

GUID de ce composant COM.

</dd> <dt>

**Contrôle**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classe \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")
</dt> </dl>

Le composant COM est un contrôle OLE.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ default \] ")
</dt> </dl>

Chemin d’accès au fichier exécutable et à l’identificateur de ressource de l’icône par défaut utilisée par la classe.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ default \] ")
</dt> </dl>

Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’un gestionnaire personnalisé 16 bits pour le composant COM. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ default \] ")
</dt> </dl>

Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’un gestionnaire personnalisé 32 bits pour le composant COM. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ par défaut \] ")
</dt> </dl>

Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’une DLL de serveur in-process 16 bits pour ce composant COM. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ default \] ")
</dt> </dl>

Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’une DLL de serveur in-process 32 bits pour ce composant COM. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**Insertable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

Le composant COM peut être inséré dans des applications de conteneur OLE.

</dd> <dt>

**JavaClass**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] »)
</dt> </dl>

Le composant COM est un composant Java.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ default \] ")
</dt> </dl>

Chemin d’accès complet incluant le nom de fichier ou uniquement le nom de fichier d’une application serveur locale 16 bits. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ default \] ")
</dt> </dl>

Chemin d’accès complet incluant le nom de fichier ou uniquement le nom de fichier d’une application serveur locale 32 bits. Le fournisseur ne retourne pas toujours le chemin d’accès complet.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ par défaut \] ")
</dt> </dl>

Nom complet de l’application COM. Elle est utilisée dans des zones telles que le champ **résultats** de la boîte de dialogue **OLE Collage spécial** .

</dd> <dt>

**ProgId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ par défaut \] ")
</dt> </dl>

Identificateur programmatique associé au composant COM. Le format d’un ProgID est <fournisseur. <version du composant. <. Il n’est pas garanti que cet identificateur soit unique.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ par défaut \] ")
</dt> </dl>

Nom abrégé de l’application COM (utilisé dans les menus et les fenêtres contextuelles).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] »)
</dt> </dl>

Modèle de thread utilisé par les classes COM in-process. Si cette propriété a la **valeur null**, aucun modèle de thread n’est utilisé. Le composant est créé sur le thread principal du client et les appels d’autres threads sont marshalés vers ce thread.

Le modèle Apartment spécifie que les composants peuvent être entrés par un et un seul thread. Les données communes détenues par ces types de serveurs d’objets doivent être protégées contre les collisions de threads, car le serveur d’objets prend en charge plusieurs composants. Chaque composant peut être entré simultanément par différents threads.

Le modèle gratuit spécifie que les composants n’imposent aucune restriction sur les threads ou le nombre de threads qui peuvent accéder à l’objet. L’objet ne peut pas contenir de données spécifiques aux threads et doit protéger ses données d’un accès simultané par plusieurs threads. Toutefois, les composants à threads libres ne sont pas accessibles directement aux threads cloisonnés, et les appels à ces derniers sont marshalés à partir du cloisonnement du client.

Lorsque les deux sont spécifiés, les composants peuvent être utilisés en mode thread cloisonné ou thread libre. Ces composants peuvent être entrés par plusieurs threads, protéger leurs données contre les collisions de threads et ne contiennent pas de données spécifiques aux threads.

Les valeurs sont :

<dl> <dd>STA</dd> <dd>Gratuit</dd> <dd>Versions</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Cloisonnement** (« Apartment »)


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Gratuit** (« gratuit »)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Les deux** (« les deux »)


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolboxBitmap32 \[ default \] ")
</dt> </dl>

Nom de module et identificateur de ressource pour une petite image bitmap (16x16) utilisée pour la face d’un bouton de barre d’outils ou de boîte à outils. Utilisé lorsque le composant COM est un contrôle OLE ou ActiveX.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ par défaut \] ")
</dt> </dl>

GUID d’un composant COM qui peut émuler des instances de ce composant.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ default \] ")
</dt> </dl>

GUID de la bibliothèque de types pour ce composant COM.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ version \[ default \] ")
</dt> </dl>

Numéro de version de cette classe COM.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgID \[ default \] ")
</dt> </dl>

Identificateur de programme cohérent pour toutes les versions du même programme.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ ClassicCOMClassSetting** est dérivée de la [**\_ comdéfinition Win32**](win32-comsetting.md).

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

[**Configuration de Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

