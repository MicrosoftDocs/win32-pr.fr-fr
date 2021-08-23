---
description: Le tableau de raccourcis contient les informations dont l’application a besoin pour créer des raccourcis sur l’ordinateur de l’utilisateur.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tableau de raccourcis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628419"
---
# <a name="shortcut-table"></a>Tableau de raccourcis

Le tableau de raccourcis contient les informations dont l’application a besoin pour créer des raccourcis sur l’ordinateur de l’utilisateur.

Le tableau de raccourcis contient les colonnes suivantes.



| Colonne                 | Type                         | Clé | Nullable |
|------------------------|------------------------------|-----|----------|
| Raccourci               | [Identificateur](identifier.md) | O   | N        |
| Répertoire\_            | [Identificateur](identifier.md) | N   | N        |
| Nom                   | [Nom du fichier](filename.md)     | N   | N        |
| Composant\_            | [Identificateur](identifier.md) | N   | N        |
| Cible                 | [Raccourci](shortcut.md)     | N   | N        |
| Arguments              | [Correct](formatted.md)   | N   | O        |
| Description            | [Text](text.md)             | N   | O        |
| Touche d’accès rapide                 | [Integer](integer.md)       | N   | O        |
| Située\_                 | [Identificateur](identifier.md) | N   | O        |
| IndexIcône              | [Integer](integer.md)       | N   | O        |
| ShowCmd                | [Integer](integer.md)       | N   | O        |
| WkDir                  | [Identificateur](identifier.md) | N   | O        |
| DisplayResourceDLL     | [Correct](formatted.md)   | N   | O        |
| DisplayResourceId      | [Integer](integer.md)       | N   | O        |
| DescriptionResourceDLL | [Correct](formatted.md)   | N   | O        |
| DescriptionResourceId  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Gestionnaires
</dt> <dd>

Valeur de clé pour cette table.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Clé externe dans la première colonne de la [table de répertoires](directory-table.md). Cette colonne spécifie le répertoire dans lequel le fichier de raccourci est créé.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom localisable du raccourci à créer.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md). Le programme d’installation utilise l’état d’installation du composant spécifié dans cette colonne pour déterminer si le raccourci est créé ou supprimé. Ce composant doit avoir un chemin d’accès de clé valide pour l’installation du raccourci. Si la colonne cible contient le nom d’une fonctionnalité, le fichier lancé par le raccourci est le fichier de clé du composant indiqué dans cet article.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif
</dt> <dd>

Cible de raccourci.

Pour un raccourci publié, cette colonne doit être une clé externe dans la première colonne du tableau des [fonctionnalités](feature-table.md). Le programme d’installation évalue l’entrée dans le champ cible en tant qu' [identificateur](identifier.md) et l’entrée doit être une clé étrangère valide dans la [table des fonctionnalités](feature-table.md). Dans ce cas, le fichier lancé par le raccourci est le fichier de clé du composant listé dans la \_ colonne composant. Lorsque le raccourci est activé, le programme d’installation vérifie que tous les composants de la fonctionnalité sont installés avant de lancer ce fichier.

Pour un raccourci non publié, le programme d’installation évalue ce champ comme une chaîne [mise en forme](formatted.md) . Le champ doit contenir un identificateur de propriété entouré de crochets ( \[ \] ), qui est développé dans le fichier ou dans un dossier désigné par le raccourci. Pour plus d’informations, consultez l' [action CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments
</dt> <dd>

Arguments de ligne de commande pour le raccourci.

Notez que la résolution des propriétés dans le champ arguments est limitée. Une propriété mise en forme en tant que \[ *propriété* \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant qui possède le raccourci est installé. Par exemple, pour résoudre la valeur correcte pour l’argument « \[ \#MyDoc.doc\] », le même processus doit installer le fichier MyDoc.doc et le composant qui possède le raccourci.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description localisable du raccourci.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Séquence
</dt> <dd>

Raccourci clavier du raccourci. L’octet de poids faible contient le code de touche virtuelle pour la clé, et l’octet de poids fort contient des indicateurs de modificateur. Il doit s’agir d’un nombre non négatif. Les auteurs des packages d’installation sont généralement recommandés pour ne pas définir cette option, car le paramètre de cette option peut ajouter des touches d’activation en double sur le Bureau d’un utilisateur. En outre, la pratique consistant à assigner des touches d’accès rapide aux raccourcis peut être problématique pour les utilisateurs qui utilisent des touches d’accès rapide pour l' [accessibilité](accessibility.md).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_
</dt> <dd>

Clé externe de la colonne de l’une des [tables d’icônes](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône
</dt> <dd>

Index d’icône pour le raccourci. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

Commande Show pour la fenêtre d’application.

Les valeurs suivantes peuvent être utilisées. les valeurs sont définies pour la fonction d’API Windows ShowWindow.



| Valeur | Signification             |
|-------|---------------------|
| 1     | \_SHOWNORMAL SW      |
| 3     | \_SHOWMAXIMIZED SW   |
| 7     | \_SHOWMINNOACTIVE SW |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Nom de la propriété qui contient le chemin d’accès du répertoire de travail du raccourci. la valeur peut utiliser le format Windows pour référencer des variables d’environnement, par exemple% USERPROFILE%. Les références sont résolues en chemin d’accès réel lorsque le programme d’installation résout le répertoire de travail pour créer le raccourci.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Ce champ contient une valeur de chaîne [mise en forme](formatted.md) pour le chemin d’accès complet au fichier exécutable portable indépendant du langage (fichier LN) qui contient les données de configuration de ressource (RC config). La chaîne mise en forme peut utiliser la \[ \# \] Convention filekey. Si ce champ contient une valeur, la colonne de nom est ignorée. Si ce champ est vide, le programme d’installation utilise la valeur dans la colonne nom. Lorsque ce champ contient une valeur, le champ **DisplayResourceId** doit également contenir une valeur, sinon l’installation échoue.

cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée. cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.

Pour plus d’informations sur l’ajout de raccourcis à une table de raccourcis pour une utilisation avec des ressources MUI, consultez [un exemple de raccourci MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Index du nom complet du raccourci. Il doit s’agir d’un nombre non négatif. Lorsque ce champ contient une valeur, le champ **DisplayResourceDLL** doit également contenir une valeur, sinon l’installation échoue.

cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée. cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Ce champ contient une valeur de chaîne [mise en forme](formatted.md) pour le chemin d’accès complet au fichier exécutable portable indépendant du langage (fichier LN) qui contient les données de configuration de ressource (RC config). La chaîne mise en forme peut utiliser la \[ \# \] Convention filekey. Si ce champ contient une valeur, la colonne de nom est ignorée. Si ce champ est vide, le programme d’installation utilise la valeur dans la colonne Description. Lorsque ce champ contient une valeur, le champ **DescriptionResourceId** doit également contenir une valeur, sinon l’installation échoue.

cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée. cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.

Pour plus d’informations sur l’ajout de raccourcis à une table de raccourcis pour une utilisation avec des ressources MUI, consultez [un exemple de raccourci MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Index du nom de description pour le raccourci. Il doit s’agir d’un nombre non négatif. Lorsque ce champ contient une valeur, le champ **DescriptionResourceDLL** doit également contenir une valeur, sinon l’installation échoue.

cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée. cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’activation d’une fonctionnalité crée un raccourci publié uniquement si l’interface IShellLink du système prend en charge la résolution du descripteur du programme d’installation. cela est pris en charge par microsoft Windows 2000 et les systèmes exécutant microsoft Internet Explorer 4,01. S’il n’est pas pris en charge, le programme d’installation crée un raccourci non publié lors de l’installation du composant de la fonctionnalité, localement ou exécuté à partir de la source.

Notez que les raccourcis publiés pointent toujours vers une application particulière, identifiés par un [**ProductCode**](productcode.md), et ne doivent pas être partagés entre les applications. Les raccourcis publiés ne fonctionnent que pour l’application la plus récemment installée, et sont supprimés lors de la suppression de cette dernière.

Cette table est référencée lorsque l' [action CreateShortcuts](createshortcuts-action.md) et l' [action RemoveShortcuts](removeshortcuts-action.md) sont exécutées.

Consultez également la propriété [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



