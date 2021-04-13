---
description: Windows Management Instrumentation (WMI) définit un ensemble de propriétés système associées à toutes les classes et instances de classes.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propriétés du système WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202279"
---
# <a name="wmi-system-properties"></a>Propriétés du système WMI

Windows Management Instrumentation (WMI) définit un ensemble de propriétés système associées à toutes les classes et instances de classes. Comme avec les classes système, les noms de propriétés système commencent par un trait de soulignement double, en les distinguant des propriétés créées par des applications ou des fournisseurs qui ne doivent pas commencer par un trait de soulignement simple ou double. Une autre façon d’identifier une propriété système consiste à utiliser la méthode [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Les propriétés système sont disponibles à tout moment, mais les valeurs peuvent être **null**. **Null** indique qu’une propriété ne s’applique pas à un objet spécifique. Toutefois, les propriétés système peuvent ne pas être disponibles tout le temps pour toutes les classes ou instances.

## <a name="system-properties"></a>Propriétés système

La liste suivante décrit les propriétés système WMI. Les exemples donnés sont tirés des propriétés système de la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , qui est décrite en bas de cette rubrique.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Type**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d’accès : lecture seule pour les instances ; lecture/écriture pour les classes

Nom de la classe.

Exemple : Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Dérivation**
</dt> <dd>

Type de données : tableau de **\_ chaînes CIM**

Type d’accès : lecture seule pour les instances et les classes

Hiérarchie de classes de l’instance ou de la classe actuelle. Le premier élément est la classe parent immédiate, le suivant est son parent, et ainsi de suite ; le dernier élément est la classe de base.

Exemple : {CIM \_ LogicalElement, CIM CIM \_ }

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Nom de la classe de niveau supérieur à partir de laquelle la classe ou l’instance est dérivée. Quand cette classe ou instance est la classe de niveau supérieur, les valeurs de **\_ \_ Dynasty** et de **\_ \_ Class** sont les mêmes.

Exemple : \_ MANAGEDSYSTEMELEMENT CIM

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genres**
</dt> <dd>

Type de données : **CIM \_ SINT32**

Type d'accès : Lecture seule

Valeur utilisée pour faire la distinction entre les classes et les instances. Cette valeur est **la \_ \_ classe de genre WBEM** (1) pour les classes, et l' **\_ \_ instance de genre WBEM** (2) pour les instances et les événements.

Exemple : 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Joint**](--namespace.md)
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Nom de l' [*espace de noms*](gloss-n.md) de la classe ou de l’instance.

Exemple : root \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_D**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Chemin d’accès complet à la classe ou à l’instance, y compris le serveur et l’espace de noms.

Exemple : \\ \\ monserveur \\ root \\ cimv2 : Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Nombre de propriétés \_**
</dt> <dd>

Type de données : **CIM \_ SINT32**

Type d'accès : Lecture seule

Nombre de propriétés qui ne sont pas du système définies pour la classe ou l’instance.

Exemple : 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Constitue**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Chemin d’accès relatif à la classe ou à l’instance.

Exemple : Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Serveurs**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Nom du serveur qui fournit la classe ou l’instance.

Exemple : MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclasse**
</dt> <dd>

Type de données **: \_ chaîne CIM**

Type d'accès : Lecture seule

Nom de la classe parent immédiate de la classe ou de l’instance.

Exemple : CIM \_ LogicalElement

</dd> </dl>

Le code PowerShell suivant récupère les propriétés de la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , qui comprend les propriétés système.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



L’exemple de code précédent retourne ce qui suit :


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
