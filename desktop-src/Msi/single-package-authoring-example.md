---
description: L’exemple de PUASample.msi est un exemple de package Windows Installer 5,0 à double usage qui peut être installé dans le contexte d’installation par utilisateur ou par ordinateur sur Windows Server 2008 R2 et Windows 7.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Exemple de création de package unique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522095"
---
# <a name="single-package-authoring-example"></a>Exemple de création de package unique

L’exemple de PUASample.msi est un exemple de package Windows Installer 5,0 à double usage qui peut être installé dans le [contexte d’installation](installation-context.md) par utilisateur ou par ordinateur sur windows Server 2008 R2 et Windows 7. Cet exemple de package suit les instructions de développement décrites dans [création de package unique](single-package-authoring.md).

## <a name="obtaining-a-copy-of-the-sample"></a>Obtention d’une copie de l’exemple

Une copie de cet exemple et d’un Windows Installer éditeur de table de base de données, Orca.exe, se trouvent dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). L’exemple et l’éditeur de table sont fournis avec le kit de développement logiciel (SDK) Windows pour Windows Server 2008 R2 et Windows 7 en tant que fichiers d’installation Windows Installer PUASample1.msi et Orca.msi.

## <a name="system-requirements"></a>Configuration requise

L’éditeur de base de données, [Orca.exe](orca-exe.md), requiert windows Server 2008 R2 et versions antérieures, ainsi que Windows 7 et versions antérieures. Le package à double usage, PUASample1.msi, peut être installé dans le [contexte d’installation](installation-context.md) par ordinateur ou par utilisateur sur windows Server 2008 R2 et Windows 7. PUASample1.msi peut être installé uniquement dans le contexte par ordinateur sur Windows Server 2008 et versions antérieures, et Windows Vista et versions antérieures. Vous pouvez installer l’éditeur de base de données pour examiner le contenu de PUASample1.msi sans installer l’exemple. Pour installer les packages de l’exemple ou de l’éditeur, vérifiez que la stratégie [DisableMSI](disablemsi.md) n’est pas définie sur une valeur qui bloque les installations d’applications.

## <a name="identifying-a-dual-purpose-package"></a>Identification d’un package Dual-Purpose

Les packages à double usage doivent initialiser la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) sur 1. Cela permet d’identifier le package comme étant en mesure de l’installer dans le contexte par ordinateur ou par utilisateur sur Windows Server 2008 R2 et Windows 7. Définissez la propriété **MSIINSTALLPERUSER** dans le package uniquement si elle a été écrite conformément aux instructions de développement décrites dans [création de package unique](single-package-authoring.md) et, si vous envisagez de fournir aux utilisateurs la possibilité d’installer le package dans le contexte par utilisateur ou par ordinateur. Un package à double usage doit également initialiser la valeur de la propriété [**ALLUSERS**](allusers.md) à 2. Cela spécifie par utilisateur comme contexte d’installation par défaut pour l’application. Si la valeur de la propriété **ALLUSERS** est différente de 2, Windows Installer ignore la propriété **MSIINSTALLPERUSER** .

Utilisez un éditeur de base de données Windows Installer, tel que [Orca.exe](orca-exe.md), pour examiner le contenu de PUASample1.msi. La table des [Propriétés](property-table.md) de l’exemple de package contient les deux entrées suivantes.

[Propriété](property-table.md) Table (partielle)

| Propriété          | Valeur |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Boîte de dialogue personnalisée pour le contexte d’installation

L' [interface utilisateur](user-interface.md) de l’exemple de package contient un exemple de boîte de dialogue personnalisée, VerifyReadyDialog, qui permet aux utilisateurs de sélectionner le contexte d’installation par utilisateur ou par ordinateur au moment de l’installation. La table [boîte de dialogue](dialog-table.md) contient un enregistrement qui décrit la boîte de dialogue VerifyReadyDialog. La valeur entrée dans le champ attributs est 39, car cette boîte de dialogue utilise les [bits de style de boîte de dialogue](dialog-style-bits.md)msidbDialogAttributesVisible (1), msidbDialogAttributesModal (2), msidbDialogAttributesMinimize (4) et msidbDialogAttributesTrackDiskSpace (32). La barre de titre de la boîte de dialogue affiche un titre donné par la valeur de la propriété [**ProductName**](productname.md) .

[Boîte de dialogue](dialog-table.md) Table (partielle) 

| Boîte de dialogue            | HCentering | VCentering | Largeur | Hauteur | Attributs | Intitulé           | \_Premier contrôle | \_Valeur par défaut du contrôle | Annuler le contrôle \_ |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | Suivant             | Annuler          |



 

La table de [contrôle](control-table.md) contient des entrées pour les [contrôles](controls.md) affichés par la boîte de dialogue VerifyReadyDialog. La boîte de dialogue affiche les contrôles [PUSHBUTTON](pushbutton-control.md) et un contrôle de [texte](text-control.md) . Tous les contrôles utilisent les [attributs de contrôle](control-attributes.md)msidbControlAttributesEnabled (2) et msidbControlAttributesVisible (1). Le contrôle InstallPerMachine utilise également l’attribut de contrôle [ElevationShield](elevationshield-attribute.md) , msidbControlAttributesElevationShield (8388608.) Cet attribut de contrôle ajoute l’icône d’élévation du [*contrôle de compte d’utilisateur*](u-gly.md) (icône bouclier) au contrôle InstallPerMachine et informe l’utilisateur que les informations d’identification UAC sont requises pour installer l’application dans le contexte par ordinateur. La valeur dans le champ de texte de la table de contrôle correspond au style de texte et au texte affiché par le contrôle. Pour plus d’informations sur l’ajout de texte à un contrôle à l’aide de styles prédéfinis, consultez la description du champ de texte dans la rubrique table de contrôle.

[Contrôle](control-table.md) Table (partielle)

| Dialogue\_          | Contrôler           | Type       | Attribut | Texte                                                   | Contrôle \_ suivant     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | Annuler            | Boutons | 3         | { \\ Tahoma10} &annuler                                    | Suivant              |
| VerifyReadyDialog | Précédente          | Boutons | 3         | { \\ Tahoma10} <<&précédent                          | Annuler            |
| VerifyReadyDialog | Suivant              | Boutons | 3         | { \\ Tahoma10} &>> suivant                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Texte       | 3         | Êtes-vous prêt à terminer l’installation interrompue ? |                   |
| VerifyReadyDialog | InstallPerUser    | Boutons | 3         | { \\ Tahoma10} installer uniquement pour &moi                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | Boutons | 8388611   | { \\ Tahoma10} installer pour &tout le monde                      | Précédente          |
| VerifyReadyDialog | Annuler            | Boutons | 3         | { \\ Tahoma10} &annuler                                    | Suivant              |



 

La table [ControlEvent,](controlevent-table.md) spécifie le [ControlEvents](control-events.md), ou les actions, que le programme d’installation effectue lorsque l’utilisateur interagit avec un contrôle. Lorsqu’un utilisateur active le bouton de sélection InstallPerUser, l’interface utilisateur affiche une boîte de dialogue OutOfDisk si la propriété [**OutOfDiskSpace**](outofdiskspace.md) a la valeur 1, définit la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) sur 1, définit la propriété [**ALLUSERS**](allusers.md) sur la valeur 2, affecte la valeur 1 à la propriété [**MSIFASTINSTALL**](msifastinstall.md) et retourne. Étant donné que la propriété **MSIFASTINSTALL** est définie, aucun point de restauration système n’est généré pour l’installation. Lorsqu’un utilisateur active le PUSHBUTTON InstallPerMachine, l’interface utilisateur affiche une boîte de dialogue OutOfDisk si la propriété **OutOfDiskSpace** est 1, définit la valeur de la propriété **ALLUSERS** sur 1 et retourne.

[ControlEvent,](controlevent-table.md) Table (partielle) 

| Dialogue\_          | contrôle\_         | Événement                 | Argument  | Condition                 | Commande |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| VerifyReadyDialog | InstallPerUser    | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerUser    | EndDialog             | Renvoie    | OutOfDiskSpace <> 1 | 5     |
| VerifyReadyDialog | InstallPerUser    | \[MSIINSTALLPERUSER\] | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| VerifyReadyDialog | InstallPerMachine | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerMachine | EndDialog             | Renvoie    | OutOfDiskSpace <> 1 | 3     |
| VerifyReadyDialog | InstallPerMachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[MSIFASTINSTALL\]    | 1         | 1                         | 4     |



 

Le contrôle InstallPerUser doit être supprimé de l’interface utilisateur de toute installation à l’aide d’une Windows Installer version antérieure à Windows Installer Windows Installer 5,0. La table [ControlCondition](controlcondition-table.md) de l’exemple de package contient quatre entrées qui désactivent et masquent le contrôle InstallPerUser si la version actuelle est inférieure à Windows Installer 5,0. La table utilise la valeur de la propriété [**VersionMsi**](versionmsi.md) et la [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md) pour définir cette condition. L’action spécifiée dans le champ action est exécutée uniquement si l’instruction dans le champ condition a la valeur true.

[ControlCondition](controlcondition-table.md) Table (partielle)

| Dialogue\_          | contrôle\_      | Action  | Condition               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | Activer  | VersionMsi >= « 5,00 » |
| VerifyReadyDialog | InstallPerUser | Désactiver | VersionMsi < « 5,00 »  |
| VerifyReadyDialog | InstallPerUser | Afficher    | VersionMsi >= « 5,00 » |
| VerifyReadyDialog | InstallPerUser | Masquer    | VersionMsi < « 5,00 »  |



 

## <a name="specifying-directory-structure"></a>Spécification de la structure de répertoires

Utilisez l’éditeur de base de données pour examiner la table de [répertoire](directory-table.md) de PUASample1.msi. L’enregistrement de la table de répertoire ayant une chaîne vide dans son \_ champ parent de répertoire représente le répertoire racine des arborescences de répertoires source et cible. Si la propriété [**targetDir**](targetdir.md) n’est pas définie, le programme d’installation définit sa valeur au moment de l’installation sur la valeur de la propriété [**ROOTDRIVE**](rootdrive.md) . Si la propriété [**SourceDir**](sourcedir.md) n’est pas définie, le programme d’installation définit sa valeur sur l’emplacement du répertoire contenant le package Windows Installer (fichier. msi). Les noms de répertoires sont spécifiés à l’aide du \| format short long.

[Répertoire](directory-table.md) Table (partielle)

| Répertoire          | Répertoire \_ parent  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | MyVendor           | Sample1 \| MSDN-PUASample1 |
| MyVendor           | ProgramFilesFolder | Msft \| Microsoft          |



 

À la source, cette table de [répertoires](directory-table.md) correspond aux chemins d’accès aux répertoires suivants.

<dl> \[SourceDir \] \\ msft \\ sample1  
\[SourceDir\]  
</dl>

Au niveau de la cible, la table de [répertoires](directory-table.md) correspond aux chemins d’accès figurant dans le tableau suivant. Le programme d’installation définit les valeurs des propriétés [**ProgramFilesFolder**](programfilesfolder.md) et [**ProgramMenuFolder**](programmenufolder.md) sur les emplacements qui dépendent du [contexte d’installation](installation-context.md) et indique si le système est la version 32 bits ou 64 bits de Windows Server 2008 R2 et Windows 7. Les chemins d’accès aux dossiers cibles varient selon que l’utilisateur sélectionne une installation par utilisateur ou par ordinateur.

| Contexte d’installation | Système                                                                              | Exemples de chemins                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 et Windows 7<br/> version 32 bits<br/>           | % ProgramFiles% \\ msft \\ sample1<br/> % ALLUSERSPROFILE% \\ des \\ \\ programmes du menu démarrer \\ de Microsoft Windows<br/>                  |
| Per-Machine          | Windows Server 2008 R2 et Windows 7<br/> version 64 bits<br/>           | % ProgramFiles (x86)% \\ msft \\ sample1<br/> % ALLUSERSPROFILE% \\ des \\ \\ programmes du menu démarrer \\ de Microsoft Windows<br/>             |
| Per-User             | Windows Server 2008 R2 et Windows 7<br/> version 32 bits ou 64 bits<br/> | % USERPROFILE% \\ AppData \\ local \\ Programs \\ msft \\ sample1<br/> % APPDATA% \\ des \\ \\ programmes du menu démarrer \\ de Microsoft Windows<br/> |



 

Les applications par utilisateur doivent être stockées dans des sous-dossiers sous le dossier programmes spécifié par la valeur de la propriété [**ProgramFilesFolder**](programfilesfolder.md) . En général, le chemin d’accès à l’application prend la forme suivante.

% LocalAppData% \\ Programs \\ *ISV Name* \\ *appname*.

Les données de configuration par utilisateur doivent être stockées dans le dossier Programs spécifié par la valeur de la propriété [**ProgramMenuFolder**](programmenufolder.md) . En règle générale, ce dossier se trouve à l’emplacement suivant.

% APPDATA% \\ des \\ \\ programmes du menu démarrer \\ de Microsoft Windows

Si vous installez des composants [de Package Windows Installer 32 bits](32-bit-windows-installer-packages.md) , utilisez la propriété [**ProgramFilesFolder**](programfilesfolder.md) et [**CommonFilesFolder**](commonfilesfolder.md) dans la table [Directory](directory-table.md) . Si vous installez des composants [de Package Windows Installer 64 bits](64-bit-windows-installer-packages.md) , utilisez les propriétés [**ProgramFiles64Folder**](programfiles64folder.md) et [**CommonFiles64Folder**](commonfiles64folder.md) . Si votre application contient des versions 32 bits et 64 bits du même composant, avec le même nom, assurez-vous que ces versions sont enregistrées dans des répertoires différents ou attribuez-leur des noms différents.

La table de [répertoire](directory-table.md) suivante fournit un exemple de disposition de répertoire compatible avec un package qui inclut des composants 32 bits et 64 bits et inclut certains composants qui sont partagés entre les applications.

| Répertoire            | Répertoire \_ parent    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | . :P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | . :P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | . : Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | MyVendor             | Sample1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATION       | ShVendor             | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| MSDN-PUASample1          |
| MyVendor             | ProgramFilesFolder   | Msft \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | Msft \| Microsoft                   |
| ShVendor             | CommonFilesFolder    | Msft \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | Msft \| Microsoft                   |
| Shrx86               | SHAREDLOCATION       | \|composants x32 32 bits            |
| Shrx64               | SHAREDLOCATIONX64    | \|composants 64 bits x64            |
| Binx86               | INSTALLLOCATION      | \|composants x32 32 bits            |
| Binx64               | INSTALLLOCATIONX64   | \|composants 64 bits x64            |
| App32                | Binx86               | MyApp \| -composants 32 bits non partagés |
| App64                | Binx64               | MyApp \| -composants 64 bits non partagés |
| Share32              | Shrx86               | \|composants partagés partagés 32 bits  |
| Share64              | Shrx64               | \|composants partagés partagés 64 bits  |



 

À la source, cette table de [répertoires](directory-table.md) correspond aux chemins d’accès aux répertoires suivants.

<dl> \[SourceDir \] Prog32 \\ msft \\ sample1 \\ x32 \\ MonApp  
\[SourceDir \] \\ fichiers communs Share32 \\ msft \\ sample1 \\ x32 \\ Shared  
\[SourceDir \] Prog64 \\ msft \\ sample1 \\ x64 \\ MonApp  
\[SourceDir \] \\ fichiers communs Share64 \\ msft \\ sample1 \\ x64 \\ partagé  
\[SourceDir \] sample1  
</dl>

Au niveau de la cible, cette table de [répertoires](directory-table.md) correspond aux chemins d’accès aux répertoires suivants. Les chemins d’accès cibles dépendent du contexte et du système d' [installation](installation-context.md) .

| Contexte d’installation | Système                                                                              | Exemples de chemins                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 et Windows 7<br/> version 32 bits<br/>           | % ProgramFiles% \\ msft \\ sample1 \\ x32 \\ MonApp<br/> % ProgramFiles% \\ fichiers communs \\ msft \\ sample1 \\ x32 \\ Shared<br/> % ProgramFiles (x86)% \\ msft \\ sample1 \\ x64 \\<br/> % ProgramFiles (x86)% \\ fichiers communs \\ msft \\ sample1 \\ x64 \\ partagés<br/> % ProgramData% \\ des \\ programmes du menu Démarrer de Microsoft Windows \\ \\ \\ sample1<br/>               |
| Per-Machine          | Windows Server 2008 R2 et Windows 7<br/> version 64 bits<br/>           | % ProgramFiles (x86)% \\ msft \\ sample1 \\ x32 \\ MonApp<br/> % ProgramFiles (x86)% \\ fichiers communs \\ msft \\ sample1 \\ x32 \\ Shared<br/> % ProgramFiles% \\ msft \\ sample1 \\ x64 \\ MyApp<br/> % ProgramFiles% \\ fichiers communs \\ msft \\ sample1 \\ x64 \\ partagé<br/> % ProgramData% \\ des \\ programmes du menu Démarrer de Microsoft Windows \\ \\ \\ sample1<br/>               |
| Per-User             | Windows Server 2008 R2 et Windows 7<br/> version 32 bits ou 64 bits<br/> | % LOCALAPPDATA% \\ Programs \\ msft \\ sample1 \\ x32 \\ MonApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ msft \\ sample1 \\ x32 \\ Shared<br/> % LOCALAPPDATA% \\ Programs \\ msft \\ sample1 \\ x64 \\ MyApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ msft \\ sample1 \\ x64 \\ Shared<br/> % APPDATA% \\ des \\ programmes du menu Démarrer de Microsoft Windows \\ \\ \\ sample1<br/> |



 

## <a name="application-registration"></a>Inscription de l’application

L' PUASample.msi ajoute une sous-clé à la clé de Registre App Paths pour l’application et effectue des inscriptions qui permettent d’enregistrer les informations de l’application dans le Registre sous cette clé. Pour plus d’informations sur les chemins d’accès des applications et l’inscription des applications, consultez [PerceivedTypes, SystemFileAssociations et inscription des applications](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) dans la section extensibilité de l' [interpréteur](https://msdn.microsoft.com/library/bb762762.aspx) de commandes dans le [Guide du développeur de l’interpréteur](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))de commandes. Au moment de l’installation, l’utilisateur prend la décision d’installer l’application dans le contexte d’installation par utilisateur ou par ordinateur. Au moment de la création du package à double usage, le développeur du package ne peut pas savoir si les inscriptions doivent être effectuées sous la \_ clé HKEY local \_ machine ou HKEY \_ Current \_ User.

Le développeur du package définit l’identificateur de fichier du fichier exécutable de l’application dans le champ fichier de la table de [fichiers](file-table.md) .

[Fichier](file-table.md) Table (partielle) 

| Fichier      | -\_      | FileName                     | FileSize | Version | Language | Attributs | Séquence |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppFile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

Les valeurs à enregistrer dans le registre peuvent être spécifiées dans le champ de valeur de la table [du Registre](registry-table.md) sous forme de chaîne [mise en forme](formatted.md) . Utilisez l’identificateur de fichier défini dans le champ fichier de la table [file](file-table.md) et la \[ \# convention *filekey* \] du type mis en forme pour spécifier la valeur par défaut de la clé de Registre Paths de l’application. L’action d' [installation](install-action.md) de niveau supérieur effectue les actions dans la table [InstallExecuteSequence](installexecutesequence-table.md) . Une fois les actions [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [InstallFinalize](installfinalize-action.md) effectuées dans ce tableau, la Windows Installer remplace la sous-chaîne mise en forme \[ \# MyAppFile \] dans la table du Registre par le chemin d’accès complet au fichier d’application.

L’exemple définit une propriété personnalisée, RegRoot, pour contenir l’emplacement de la clé racine et utilise une action personnalisée pour réinitialiser la valeur de la propriété si l’utilisateur choisit une installation par ordinateur. Utilisez la propriété personnalisée, RegRoot, dans toutes les valeurs de chaîne mises en forme qui référencent l’emplacement racine. Dans la table des [Propriétés](property-table.md) , le package PUASample.msi définit la propriété personnalisée et définit la valeur de REGROOT sur HKCU. Cela initialise la valeur de la propriété pour le contexte d’installation par utilisateur, le contexte par défaut recommandé pour les packages à double usage.

[Propriété](property-table.md) Table (partielle)

| Propriété | Valeur |
|----------|-------|
| RegRoot  | HKCU  |



 

Dans la table [CustomAction](customaction-table.md) , le package définit une action personnalisée nommée Set \_ RegRoot \_ HKLM. La valeur dans le champ type identifie cela comme une action personnalisée [51 de type action](custom-action-type-51.md) personnalisée standard. La signification des champs source et cible dans la table CustomAction dépend du type d’action personnalisé. Pour plus d’informations sur les types standard d’actions personnalisées, consultez types d’actions [personnalisées](summary-list-of-all-custom-action-types.md). Le champ source de l' \_ \_ action personnalisée HKLM Set RegRoot spécifie que la valeur de la propriété RegRoot. Si le programme d’installation effectue \_ l' \_ action personnalisée de définition de RegRoot HKLM, cette opération réinitialise la valeur de la propriété REGROOT à HKLM.

[CustomAction](customaction-table.md) Table (partielle)

| Action             | Type | Source      | Cible |
|--------------------|------|-------------|--------|
| Définir \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

L’action d' [installation](install-action.md) de niveau supérieur effectue les actions dans la table [InstallExecuteSequence](installexecutesequence-table.md) , dans la séquence spécifiée dans le champ séquence de cette table. La valeur créée dans le champ séquence pour l' \_ \_ action personnalisée RegRoot HKLM (1501) spécifie que cette action personnalisée doit être exécutée après l’action [InstallInitialize](installinitialize-action.md) (1500) et avant l’action [ProcessComponents](processcomponents-action.md) (1600.) Cette séquence garantit que l’enregistrement de l' \_ \_ action personnalisée HKLM Set RegRoot est évalué au moment de l’installation. Pour plus d’informations sur la séquence d’actions recommandée dans la table InstallExecuteSequence, consultez la rubrique [InstallExecuteSequence suggérée](suggested-installexecutesequence.md) . La [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md) créée dans le champ condition spécifie que l' \_ \_ action HKLM Set RegRoot doit être exécutée uniquement si la valeur de la propriété [**ALLUSERS**](allusers.md) est égale à 1 au moment de l’installation. Une valeur de propriété **ALLUSERS** de 1 spécifie une installation par ordinateur.

[InstallExecuteSequence](installexecutesequence-table.md) Table (partielle)

| Action             | Condition  | Séquence |
|--------------------|------------|----------|
| Définir \_ RegRoot \_ HKLM | ALLUSERS = 1 | 1501     |



 

Les enregistrements suivants dans la table [du Registre](registry-table.md) effectuent les inscriptions si le composant ProductComponent est installé. La valeur-1 dans le champ racine est requise pour effectuer l’inscription sous HKEY \_ local \_ machine pour une installation par utilisateur et sous HKEY \_ Current \_ User pour une installation par utilisateur. L’enregistrement avec une chaîne vide dans le champ Registry ajoute une sous-clé pour l’application sous la clé de Registre chemins et définit la valeur « (par défaut) » sur le chemin d’accès complet du fichier exécutable de l’application. L’inscription MyAppPathAlias mappe le fichier exécutable à un alias d’application et permet à l’application d’être lancée si l’utilisateur tape l’alias « puapct » à l’invite de ligne de commande. L’inscription MyAppPathRegistration mappe le nom du fichier exécutable sur le chemin d’accès complet du fichier.



| Registre              | Root | Clé                                                                     | Nom | Valeur                                                                            | Composant        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Logiciel \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[RegRoot \] \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ path \\PUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | Logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ path \\PUAPCT.exe     |      | \[\#MyAppFile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | Logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ path \\PUASample1.exe |      | \[\#MyAppFile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>Annulation de l’inscription automatique

L' PUASample.msi effectue des inscriptions qui permettent à l’utilisateur de l’application d’empêcher le lancement de l' [exécution automatique du matériel](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) pour les appareils sélectionnés. Pour plus d’informations sur l’inscription d’un gestionnaire pour annuler l’exécution automatique en réponse à un événement, consultez la rubrique [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](/previous-versions//cc144208(v=vs.85)) dans la section extensibilité de l' [interpréteur](https://msdn.microsoft.com/library/bb762762.aspx) de commandes dans le [Guide du développeur de l’interpréteur](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))de commandes. L’enregistrement suivant inscrit le gestionnaire spécifié dans le champ nom lorsque le composant ProductComponent est installé. La valeur-1 dans le champ racine est obligatoire pour spécifier l’Windows Installer que l’inscription doit être redirigée vers un emplacement qui dépend du contexte d’installation.

[Registre](registry-table.md) Tableau 

| Registre                     | Root | Clé                                                                                             | Nom                                 | Valeur | Composant        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | LOGICIEL \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ cancelautoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>Aperçu du gestionnaire d’aperçus

L' PUASample.msi effectue les inscriptions nécessaires à l’installation d’un [Gestionnaire d’aperçus](../shell/preview-handlers.md) qui permet une version d’évaluation en lecture seule des fichiers. PUA sans lancer l’application. Pour plus d’informations sur l’inscription des gestionnaires d’aperçus, consultez la rubrique [inscription des gestionnaires d’aperçus](../shell/how-to-register-a-preview-handler.md) dans la section extensibilité de l' [interpréteur](https://msdn.microsoft.com/library/bb762762.aspx) de commandes dans le Guide du développeur de l' [interpréteur](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))de commandes. Les enregistrements suivants de la table [du Registre](registry-table.md) inscrivent le gestionnaire lors de l’installation du composant ProductComponent. La valeur-1 dans le champ racine est obligatoire pour spécifier l’Windows Installer que l’inscription doit être redirigée vers un emplacement qui dépend du contexte d’installation.

[Registre](registry-table.md) Tableau

| Registre                       | Root | Clé                                                                              | Nom                                   | Valeur                                        | Composant        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | Classes de logiciels \\ \\ . PUA                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Logiciel \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Gestionnaire d’aperçus de TEST Microsoft Windows PUA   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | Classes de logiciels \\ \\ puafile \\ shellex \\ {8895b1c6-B41F-4c1c-A562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Per-User exemple de gestionnaire d’aperçus application 1 | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32,-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | Icône                                   | notepad.exe, 2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ThreadingModel                         | STA                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 |                                        | \#%% SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | Classes de logiciels \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 
