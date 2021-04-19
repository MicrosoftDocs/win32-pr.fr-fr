---
description: Les tables suivantes sont requises dans un module de fusion standard.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Tables de base de données de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535513"
---
# <a name="merge-module-database-tables"></a>Tables de base de données de module de fusion

Les tables suivantes sont requises dans un module de fusion standard.



| Nom de la table                                       | Commentaire                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Composant](component-table.md)                 | SOUHAITÉE                                                                                       |
| [Directory](directory-table.md)                 | SOUHAITÉE                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | SOUHAITÉE                                                                                       |
| [File](file-table.md)                           | SOUHAITÉE                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | SOUHAITÉE Fusionné dans la base de données du programme d’installation. Répertorie les informations identifiant un module de fusion. |
| [ModuleComponents](modulecomponents-table.md)   | SOUHAITÉE Fusionné dans la base de données du programme d’installation. Répertorie tous les composants du module de fusion.     |



 

Les tables suivantes se trouvent uniquement dans des modules de fusion ou d’autres bases de données de programme d’installation qui ont déjà été combinées avec un module de fusion.



| Nom de la table                                     | Commentaire                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | Fusionné dans la base de données du programme d’installation. Répertorie les autres modules de fusion requis par ce module de fusion.                |
| [ModuleExclusion](moduleexclusion-table.md)   | Fusionné dans la base de données du programme d’installation. Répertorie les autres modules de fusion qui ne sont pas compatibles avec ce module de fusion. |



 

Les tables ModuleSequence suivantes se trouvent uniquement dans les modules de fusion.



| Nom de la table                                                             | Commentaire                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | Fusionne des actions dans la [table AdminUISequence](adminuisequence-table.md).               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | Fusionne des actions dans la [table AdminExecuteSequence](adminexecutesequence-table.md).     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | N’utilisez pas cette table. Pour plus d’informations, consultez la [table AdvtUISequence](advtuisequence-table.md). |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | Fusionne des actions dans la [table AdvtExecuteSequence](advtexecutesequence-table.md).       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | Répertorie les tables du module qui ne sont pas fusionnées dans le fichier. msi.                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | Fusionne des actions dans la [table InstallUISequence](installuisequence-table.md).           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | Fusionne des actions dans la [table InstallExecuteSequence](installexecutesequence-table.md). |



 

Les tables suivantes sont requises dans chaque module de fusion configurable. Mergemod.dll 2,0 ou version ultérieure est requis pour créer un module de fusion configurable. Pour plus d’informations, consultez [modules de fusion configurables](configurable-merge-modules.md).



| Nom de la table                                                 | Commentaire                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Table ModuleSubstitution](modulesubstitution-table.md)   | SOUHAITÉE Cette table n’est pas fusionnée dans la base de données d’installation cible. Spécifie les champs configurables dans la base de données cible et fournit un modèle pour la configuration de chaque champ. |
| [Table ModuleConfiguration](moduleconfiguration-table.md) | SOUHAITÉE Cette table n’est pas fusionnée dans la base de données d’installation cible. Identifie les attributs configurables du module.                                                                 |



 

Les tables de programme d’installation suivantes ne peuvent pas se produire dans un module de fusion standard.

-   [BBControl](bbcontrol-table.md)
-   [Blanc](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [Error](error-table.md)
-   [Fonctionnalité](feature-table.md)
-   [Table LaunchCondition](launchcondition-table.md)
-   [Média](media-table.md)
-   [Patch](patch-table.md)
-   [Mettre à niveau](upgrade-table.md)

Les tables de programme d’installation suivantes sont facultatives dans les modules de fusion.

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Classe](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [Contrôle](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Dialogue](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [DuplicateFile](duplicatefile-table.md)
-   [Environment](environment-table.md)
-   [EventMapping](eventmapping-table.md)
-   [Extension](extension-table.md)
-   [Police](font-table.md)
-   [Icône](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [MIME](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCAttribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [Table ProgID](progid-table.md)
-   [Propriété](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Table du Registre](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [ServiceInstall](serviceinstall-table.md)
-   [Raccourci](shortcut-table.md)
-   [Signature](signature-table.md)
-   [TextStyle](textstyle-table.md)
-   [Exportation](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verbe](verb-table.md)

 

 



