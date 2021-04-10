---
description: La \_ classe WMI Win32 PrinterConfiguration représente la configuration d’un périphérique d’impression. Cela comprend des fonctionnalités telles que la résolution, la couleur, les polices et l’orientation.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950757"
---
# <a name="win32_printerconfiguration-class"></a>\_Classe PrinterConfiguration Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PrinterConfiguration** représente la configuration d’un périphérique d’impression. Cela comprend des fonctionnalités telles que la résolution, la couleur, les polices et l’orientation.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PrinterConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PrinterConfiguration** a ces propriétés.

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre de bits utilisés pour représenter la couleur dans cette configuration (bits par pixel). Cette propriété est obsolète. Utilisez plutôt des propriétés dans les classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) pour déterminer comment la couleur est représentée.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**Copies assemblées**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, les pages imprimées doivent être assemblées. Pour assembler est d’imprimer l’intégralité du document avant d’imprimer la copie suivante, au lieu d’imprimer chaque page du document le nombre de fois requis.

Cette propriété est ignorée sauf si le pilote d’imprimante indique la prise en charge du classement.

</dd> <dt>

**Color**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Couleur du document. Certaines imprimantes couleur ont la possibilité d’imprimer à l’aide d’un vrai noir au lieu d’une combinaison de cyan, magenta et jaune (CMJ). Cela crée généralement un texte plus sombre et plus clair pour les documents. Cette option est utile uniquement pour les imprimantes couleur qui prennent en charge l’impression noir.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Monochrome (vrai noir)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Couleur

</dd> </dl>

</dd> <dt>

**Copies**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de copies à imprimer. Le pilote d’imprimante doit prendre en charge l’impression de copies à plusieurs pages.

Exemple : 2

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

**DeviceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom convivial de l’imprimante. Ce nom est unique pour le type d’imprimante et peut être tronqué en raison des limitations de la chaîne à partir de laquelle il est dérivé.

Exemple : « PCL/HP LaserJet »

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le périphérique d’affichage est de couleur ou monochrome et si le type d’analyse est non entrelacé ou entrelacé. Cette propriété est obsolète. Utilisez plutôt des propriétés d’affichage telles que la propriété **DisplayType** de la classe **Win32 \_ desktopmonitor** .

</dd> <dt>

**DisplayFrequency**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Affiche la fréquence de rafraîchissement verticale. La fréquence d’actualisation d’une analyse est le nombre de fois où l’écran est redessiné par seconde (fréquence). Cette propriété est obsolète. Au lieu de cela, utilisez les propriétés de la classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de trame de l’imprimante. Cette propriété peut supposer des valeurs prédéfinies de 1 à 5, ou des valeurs définies par le pilote comprises entre 6 et 256. Le tramage en ligne est une méthode de tramage spéciale qui produit des bordures bien définies entre les mises à l’échelle en noir, blanc et gris. Elle ne convient pas aux images qui incluent des diplômes continus en intensité et en teinte, tels que des photographies numérisées.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aucun tramage

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pinceau épais

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Pinceau fin

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Art en ligne

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5,5**


</dt> <dd>

Grayscale (Nuances de gris)

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de version du pilote d’imprimante Windows. Les numéros de version sont créés et gérés par le fabricant du pilote.

</dd> <dt>

**Duplex**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’impression est effectuée des deux côtés. Si la **valeur est false**, l’impression est effectuée sur un seul côté du média.

</dd> <dt>

**NomFormulaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non pris en charge.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (points par pouce)
</dt> </dl>

Résolution d’impression en points par pouce le long de l’axe x (largeur) du travail d’impression (similaire à la propriété **XResolution** obsolète). Cette valeur est définie uniquement lorsque la propriété **PrintQuality** de cette classe est positive.

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur spécifique de l’une des trois méthodes de correspondance des couleurs possibles (appelées intentions) qui doit être utilisée par défaut. Les applications ICM établissent des intentions à l’aide des fonctions ICM. Cette propriété peut supposer des valeurs prédéfinies de 1 à 3, ou des valeurs définies par le pilote, comprises entre 4 et 256. Les applications non-ICM peuvent utiliser cette valeur pour déterminer comment l’imprimante gère les travaux d’impression couleur.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Saturation

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Comparez

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Couleur exacte

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mode de gestion de l’ICM. Pour une application non-ICM, cette propriété détermine si ICM est activé ou désactivé. Pour les applications ICM, le système examine cette propriété pour déterminer quelle partie du système d’ordinateur gère la prise en charge d’ICM.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Désactivé

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Pilote de périphérique

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Appareil

</dd> </dl>

</dd> <dt>

**LogPixels**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre de pixels par pouce logique. Cette propriété obsolète est valide uniquement avec les appareils qui fonctionnent avec des pixels, ce qui exclut les appareils tels que les imprimantes. Aucune valeur de remplacement ne s’applique aux imprimantes.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de support sur lequel l’imprimante imprime. La propriété peut être définie sur une valeur prédéfinie ou sur une valeur définie par le pilote supérieure ou égale à 256.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

standard

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Transparence

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Brillance

</dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nom de l’imprimante à laquelle cette configuration est associée. Cette valeur correspond à la propriété **Name** de l’instance d' [**\_ imprimante Win32**](win32-printer.md) associée.

</dd> <dt>

**Orientation**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Impression de l’orientation du papier.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Portrait

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Paysage

</dd> </dl>

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre)
</dt> </dl>

Longueur du papier. Pour déterminer la taille du papier en pouces, divisez cette valeur par 254.

Exemple : 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille du papier. Les tailles possibles se trouvent dans la propriété **PaperSizesSupported** de la classe [**\_ Printer Win32**](win32-printer.md) associée.

Exemple : « a4 ou lettre ».

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre)
</dt> </dl>

Largeur du papier. Pour déterminer la taille du papier en pouces, divisez cette valeur par 254.

Exemple : 2159

</dd> <dt>

**PelsHeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété n'est pas prise en charge.

</dd> <dt>

**PelsWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété n'est pas prise en charge.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Un des quatre niveaux de qualité du travail d’impression. Si une valeur positive est spécifiée, la qualité est mesurée en points par pouce.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Brouillon

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**2**


</dt> <dd>

Faible

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**3**


</dt> <dd>

Moyenne

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

Élevé

</dd> </dl>

</dd> <dt>

**Mise à l’échelle**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (pourcentage)
</dt> </dl>

Facteur par lequel la sortie imprimée doit être mise à l’échelle. Par exemple, une échelle de 75 réduit la sortie d’impression à 3/4 de sa hauteur et de sa largeur d’origine.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de version des données d’initialisation pour l’appareil associé à l’imprimante Windows.

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment les polices TrueType doivent être imprimées.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)


</dt> <dd>

Imprime les polices TrueType en tant que graphiques. Il s’agit de l’action par défaut pour les imprimantes matricielles.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Télécharger** (2)


</dt> <dd>

Télécharge les polices TrueType en tant que polices logicielles. Il s’agit de l’action par défaut pour les imprimantes qui utilisent le langage de contrôle d’imprimante (PCL).

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Remplacer** (3)


</dt> <dd>

Remplace les polices de l’appareil par des polices TrueType. Il s’agit de l’action par défaut pour les imprimantes PostScript.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (points par pouce)
</dt> </dl>

Résolution d’impression le long de l’axe y (hauteur) du travail d’impression (similaire à la propriété **YResolution** obsolète). Cette valeur est définie uniquement lorsque la propriété **PrintQuality** de cette classe est positive.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété est obsolète. Utilisez la propriété **HorizontalResolution** à la place.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété est obsolète. Utilisez plutôt la propriété **VerticalResolution** .

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ PrinterConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).

**Vue d’ensemble**

Avant de pouvoir déterminer comment distribuer et utiliser au mieux vos ressources d’impression, vous devez avoir une connaissance détaillée de ces ressources. Par exemple, le service A peut avoir seulement trois imprimantes par rapport à cinq imprimantes dans le département B. Toutefois, si les imprimantes du service A peuvent imprimer 20 pages par minute et que les imprimantes du département B peuvent imprimer seulement 5 pages par minute, les utilisateurs du service A ont en fait davantage de capacité d’impression. Sans connaître les fonctionnalités détaillées de ces imprimantes, vous pouvez conclure par erreur que le service A est limité à la capacité d’impression et, par conséquent, acheter des imprimantes supplémentaires qui finissent par ne plus être utilisées.

WMI comprend deux classes, [**Win32 \_ Printer**](win32-printer.md) et **Win32 \_ PrinterConfiguration**, qui peuvent être utilisées pour retourner des informations détaillées sur toutes les imprimantes installées sur un ordinateur.

## <a name="examples"></a>Exemples

L’exemple de code suivant récupère des informations sur l’imprimante.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](./cim-setting.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
