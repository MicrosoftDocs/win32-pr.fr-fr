---
description: La table des composants répertorie les composants et contient les colonnes suivantes.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Table des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1888628137fcf07cab07d011325ff685809cff68
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474945"
---
# <a name="component-table"></a>Table des composants

La table des composants répertorie les composants et contient les colonnes suivantes.



| Colonne      | Type                         | Clé : | Nullable |
|-------------|------------------------------|-----|----------|
| Composant   | [Identificateur](identifier.md) | O   | N        |
| ComponentId | [GUID](guid.md)             | N   | O        |
| Répertoire\_ | [Identificateur](identifier.md) | N   | N        |
| Attributs  | [Integer](integer.md)       | N   | N        |
| Condition   | [Condition](condition.md)   | N   | O        |
| KeyPath     | [Identificateur](identifier.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>-
</dt> <dd>

Identifie l’enregistrement du composant.

Clé de table primaire.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

GUID de chaîne unique à ce composant, version et langue.

Notez que les lettres de ces GUID doivent être en majuscules. Les utilitaires tels que GUIDGEN peuvent générer des GUID contenant des lettres minuscules. Les lettres minuscules doivent être remplacées par des majuscules pour que ces GUID de code de composant soient valides.

Si cette colonne est null, le programme d’installation n’inscrit pas le composant et le composant ne peut pas être supprimé ou réparé par le programme d’installation. Cela peut être intentionnellement effectué si le composant n’est nécessaire que pendant l’installation, par exemple une action personnalisée qui nettoie les fichiers temporaires ou supprime un ancien produit. Cela peut également être utile lors de la copie de fichiers de données sur l’ordinateur d’un utilisateur qui n’ont pas besoin d’être inscrits.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Clé externe d’une entrée dans la [table de répertoires](directory-table.md). Il s’agit d’un nom de propriété dont la valeur contient le chemin d’accès réel, qui peut être défini soit par l' [action AppSearch](appsearch-action.md) , soit par le paramètre par défaut obtenu à partir de la table de répertoire.

Les développeurs doivent éviter de créer des composants qui placent des fichiers dans l’un des dossiers de profil utilisateur. Ces fichiers ne sont pas disponibles pour tous les utilisateurs dans des situations multi-utilisateurs et peuvent amener le programme d’installation à afficher définitivement le composant comme nécessitant une réparation.

Clé externe vers la colonne une de la table de répertoires.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Cette colonne contient un indicateur binaire qui spécifie les options d’exécution à distance. Ajoutez le bit indiqué à la valeur totale de la colonne pour inclure une option.

> [!Note]  
> Dans le cas d’un fichier .msi téléchargé à partir d’un emplacement Web, les indicateurs d’attribut ne doivent pas être définis de façon à autoriser l’exécution d’un composant à partir de la source. il s’agit d’une limitation de la Windows Installer et peut retourner un état de fonctionnalité de INSTALLSTATE \_ BADCONFIG.

 




| Indicateur de bit | 
|----------|
| <dl><dt><strong>msidbComponentAttributesLocalOnly</strong></dt><dt>0</dt><dt>0x0000</dt></dl> Le composant ne peut pas être exécuté à partir de la source. Définissez ce bit pour tous les composants appartenant à une fonctionnalité pour empêcher l’exécution de la fonctionnalité à partir du réseau ou de l’exécution à partir de la source. Notez que si une fonctionnalité ne possède aucun composant, la fonctionnalité affiche toujours exécuter à partir de la source et exécuter à partir de mon ordinateur comme options valides.<br /> | 
| <dl><dt><strong>msidbComponentAttributesSourceOnly</strong></dt><dt>1</dt><dt>0x0001</dt></dl> Le composant ne peut être exécuté qu’à partir de la source. Définissez ce bit pour tous les composants appartenant à une fonctionnalité pour empêcher l’exécution de la fonctionnalité à partir de-My-Computer. Notez que si une fonctionnalité ne possède aucun composant, la fonctionnalité affiche toujours exécuter à partir de la source et exécuter à partir de mon ordinateur comme options valides.<br /> | 
| <dl><dt><strong>msidbComponentAttributesOptional</strong></dt><dt>2</dt><dt>0x0002</dt></dl> Le composant peut s’exécuter localement ou à partir de la source.<br /> | 
| <dl><dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt><dt>4</dt><dt>0x0004</dt></dl> Si ce bit est défini, la valeur dans la colonne keyPath est utilisée comme clé dans la <a href="registry-table.md">table du Registre</a>. Si le champ de valeur de l’enregistrement correspondant dans la table de Registre est null, le champ de nom de cet enregistrement ne doit pas contenir « + », « - » ou « * ». Pour plus d’informations, consultez la description du champ Name dans la <a href="registry-table.md">table Registry</a>.<br /> La définition de ce bit est recommandée pour les entrées de Registre écrites dans la ruche HKCU. Cela permet de s’assurer que le programme d’installation écrit les entrées de Registre HKCU nécessaires lorsqu’il y a plusieurs utilisateurs sur le même ordinateur.<br /> | 
| <dl><dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt><dt>8</dt><dt>0x0008</dt></dl> Si ce bit est défini, le programme d’installation incrémente le nombre de références dans le registre de DLL partagé du fichier de clé du composant. Si ce bit n’est pas défini, le programme d’installation incrémente le décompte de références uniquement si le nombre de références existe déjà.<br /> | 
| <dl><dt><strong>msidbComponentAttributesPermanent</strong></dt><dt>16</dt><dt>0x0010</dt></dl> Si ce bit est défini, le programme d’installation ne supprime pas le composant pendant une désinstallation. le programme d’installation inscrit un client système supplémentaire pour le composant dans les paramètres du registre Windows Installer.<br /> | 
| <dl><dt><strong>msidbComponentAttributesODBCDataSource</strong></dt><dt>32</dt><dt>0x0020</dt></dl> Si ce bit est défini, la valeur dans la colonne keyPath est une clé dans la <a href="odbcdatasource-table.md">table ODBCDataSource</a>.<br /> | 
| <dl><dt><strong>msidbComponentAttributesTransitive</strong></dt><dt>64</dt><dt>0x0040</dt></dl> Si ce bit est défini, le programme d’installation réévalue la valeur de l’instruction dans la colonne condition lors de la réinstallation. Si la valeur était précédemment false et a été remplacée par true, le programme d’installation installe le composant. Si la valeur était précédemment true et a été remplacée par false, le programme d’installation supprime le composant même si le composant a d’autres produits comme clients.<br /> Ce bit ne doit être défini que pour les composants transitifs. Consultez <a href="using-transitive-components.md">utilisation des composants transitives</a>.<br /> | 
| <dl><dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt><dt>128</dt><dt>0x0080</dt></dl> Si ce bit est défini, le programme d’installation n’installe pas ou ne réinstalle pas le composant si un fichier de chemin d’accès de clé ou une entrée de registre de chemin d’accès de clé pour le composant existe déjà. L’application s’inscrit elle-même en tant que client du composant.<br /> Utilisez cet indicateur uniquement pour les composants qui sont enregistrés par la table du Registre. N’utilisez pas cet indicateur pour les composants enregistrés par l' <a href="appid-table.md">AppID</a>, la <a href="class-table.md">classe</a>, l' <a href="extension-table.md">extension</a>, le <a href="progid-table.md">ProgID</a>, le <a href="mime-table.md">MIME</a>et les <a href="verb-table.md">tables de verbes</a>.<br /> | 
| <dl><dt><strong>msidbComponentAttributes64bit</strong></dt><dt>256</dt><dt>0x0100</dt></dl> Définissez ce bit sur marquer comme un composant 64 bits. Cet attribut facilite l’installation des packages qui incluent des composants 32 bits et 64 bits. Si ce bit n’est pas défini, le composant est inscrit en tant que composant 32 bits.<br /> S’il s’agit d’un composant 64 bits qui remplace un composant 32 bits, définissez ce bit et attribuez un nouveau GUID dans la colonne ComponentId.<br /> | 
| <dl><dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt><dt>512</dt><dt>0x0200</dt></dl> Définissez ce bit pour désactiver la <a href="/windows/desktop/WinProg64/registry-reflection">réflexion du Registre</a> sur toutes les clés de Registre existantes et nouvelles affectées par ce composant. si ce bit est défini, le Windows Installer appelle le <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> sur chaque clé à laquelle le composant accède. ce bit est disponible avec la version 4,0 de Windows Installer. Ce bit est ignoré sur les systèmes 32 bits. ce bit est ignoré sur les versions 64 bits de Windows XP.<br /><blockquote>[!Note]<br />les applications 32 bits Windows s’exécutant sur l’émulateur de Windows 64 bits (WOW64) font référence à une vue différente du registre que les applications 64 bits. La réflexion du Registre copie certaines valeurs du Registre entre ces deux vues du Registre.</blockquote><br /><br /> | 
| <dl><dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt><dt>1024</dt><dt>0x0400</dt></dl> Définissez ce bit pour un composant dans un package correctif afin d’éviter de laisser des composants orphelins sur l’ordinateur. si un patch suivant est installé, marqué avec la valeur <strong>msidbPatchSequenceSupersedeEarlier</strong> dans sa table <a href="msipatchsequence-table.md">MsiPatchSequence</a> pour remplacer le premier correctif, Windows Installer 4,5 et versions ultérieures peuvent annuler l’inscription et désinstaller les composants marqués avec la valeur <strong>msidbComponentAttributesUninstallOnSupersedence</strong> . Si le composant n’est pas marqué avec ce bit, l’installation d’un correctif de remplacement peut sortir d’un composant inutilisé sur l’ordinateur.<br /> La définition de la propriété <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> a le même effet que la définition de ce bit pour tous les composants.<br /><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 et versions antérieures</a>:</strong> la valeur <strong>msidbComponentAttributesUninstallOnSupersedence</strong> n’est pas prise en charge et est ignorée.<br /><br /> | 
| <dl><dt><strong>msidbComponentAttributesShared</strong></dt><dt>2048</dt><dt>0x0800</dt></dl> Si un composant est marqué avec cette valeur d’attribut dans au moins un package installé sur le système, le programme d’installation traite le composant comme étant marqué dans tous les packages. si un package qui partage le composant marqué est désinstallé, Windows Installer 4,5 peut continuer à partager la version la plus récente du composant sur le système, même si cette version la plus récente a été installée par le package en cours de désinstallation. <br /> Si la stratégie DisableSharedComponent est définie sur 1, aucun package n’obtient la fonctionnalité de composant partagé activée par ce bit.<br /><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 et versions antérieures</a>:</strong> la valeur <strong>msidbComponentAttributesShared</strong> n’est pas prise en charge et est ignorée.<br /><br /> | 




 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Cette colonne contient une instruction conditionnelle qui peut contrôler si un composant est installé. Si la condition est null ou a la valeur true, le composant est activé. Si la condition prend la valeur false, le composant est désactivé et n’est pas installé.

Le champ condition active ou désactive un composant uniquement pendant l' [action CostFinalize](costfinalize-action.md). Pour activer ou désactiver un composant après CostFinalize, vous devez utiliser une action personnalisée ou la [ControlEvent,](doaction-controlevent.md) de script pour appeler [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea).

Notez que, sauf si le bit transitif dans la colonne attributs est défini pour un composant, le composant reste activé une fois installé, même si l’instruction conditionnelle dans la colonne condition prend la valeur false lors d’une installation de maintenance ultérieure du produit.

La colonne condition de la table Component accepte les expressions conditionnelles qui contiennent des références aux États installés des fonctionnalités et des composants. Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath
</dt> <dd>

Cette valeur pointe vers un fichier ou dossier appartenant au composant que le programme d’installation utilise pour détecter le composant. Deux composants ne peuvent pas partager la même valeur de chemin d’accès de clé. La valeur de cette colonne est également le chemin d’accès retourné par la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .

Si la valeur n’est pas null, keyPath est soit une clé primaire dans le [Registre](registry-table.md), [ODBCDataSource](odbcdatasource-table.md)ou des [tables de fichiers](file-table.md) en fonction de la valeur de l’attribut. Si keyPath a la valeur null, le dossier de la \_ colonne Directory est utilisé comme chemin d’accès de la clé.

Étant donné que les dossiers créés par le programme d’installation sont supprimés lorsqu’ils sont vides, vous devez créer une entrée dans la [table CreateFolder](createfolder-table.md) pour installer un composant qui se compose d’un dossier vide.

notez que si un composant Windows Installer contient un fichier ou une clé de registre protégés par [Protection des ressources Windows](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) ou un fichier protégé par Windows protection de fichier (WFP), cette ressource doit être utilisée comme chemin d’accès au keypath du composant. dans ce cas, Windows Installer n’installe pas, ne met pas à jour ou ne supprime pas le composant. Vous ne devez pas inclure de ressources protégées dans un package d’installation. au lieu de cela, vous devez utiliser les [mécanismes de remplacement des ressources pris en charge](/windows/desktop/Wfp/supported-file-replacement-mechanisms) pour Protection des ressources Windows. pour plus d’informations, consultez [utilisation de Windows Installer et Protection des ressources Windows](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la relation entre les composants et les fonctionnalités, consultez [table](feature-table.md)des fonctionnalités.

Le programme d’installation effectue le suivi des DLL partagées indépendamment du nombre de références de DLL partagées dans le registre. Si un nombre de références pour une DLL partagée existe dans le registre, le programme d’installation incrémente toujours le nombre lors de l’installation du fichier et le décrémente lors de sa désinstallation. Si **msidbComponentAttributesSharedDllRefCount** n’est pas défini et que le décompte de références n’existe pas encore, le programme d’installation n’en crée pas. Notez que le nombre de références SharedDLLs dans le Registre est incrémenté pour tous les fichiers installés dans le dossier système.

Si **msidbComponentAttributesSharedDllRefCount** n’est pas défini, une autre application peut supprimer le composant même s’il est toujours nécessaire. Pour voir comment cela peut se produire, examinez le scénario suivant :

-   Une application qui utilise le programme d’installation installe un composant partagé.
-   Le bit **msidbComponentAttributesSharedDllRefCount** n’est pas défini et il n’y a aucun nombre de références. Par conséquent, le programme d’installation ne commence pas un décompte de références.
-   Une application héritée qui partage ce composant et n’utilise pas le programme d’installation est installé.
-   L’application héritée crée et incrémente un décompte de références pour le composant partagé.
-   L’application héritée est désinstallée.
-   Le nombre de références pour le composant partagé est décrémenté à zéro et le composant est supprimé.
-   L’application qui utilise le programme d’installation n’a plus accès au composant.

Pour éviter ce comportement, définissez **msidbComponentAttributesSharedDllRefCount**.

Notez que les composants des services système ne doivent pas être spécifiés en tant que source d’exécution sans être spécifiquement conçus pour une telle utilisation. Pour plus d’informations, consultez la [table ServiceInstall](serviceinstall-table.md) .

Notez que les attributs permettant l’installation de l’exécution à partir de la source ne doivent jamais être définis pour les composants qui contiennent des bibliothèques de liens dynamiques qui vont dans le dossier système. En effet, si l’état d’installation du composant devient exécuter à partir de la source en suivant une fonctionnalité ou en étant défini dans l’interface utilisateur, les appels suivants à **LoadLibrary** sur la dll échouent.

Voir aussi [contrôle des États de sélection des fonctionnalités](controlling-feature-selection-states.md).

## <a name="validation"></a>Validation

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

