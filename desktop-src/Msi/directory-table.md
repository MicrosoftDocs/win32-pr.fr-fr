---
description: La table Directory spécifie la disposition des répertoires pour le produit. Chaque ligne de la table indique un répertoire à la fois au niveau de la source et de la cible.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Table de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19e9b5994062ac55564799854fc36016fc6ddb9887bc36aa9a94652ef31aeb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947343"
---
# <a name="directory-table"></a>Table de répertoire

La table Directory spécifie la disposition des répertoires pour le produit. Chaque ligne de la table indique un répertoire à la fois au niveau de la source et de la cible.

La table Directory contient les colonnes suivantes.



| Colonne            | Type                         | Clé | Nullable |
|-------------------|------------------------------|-----|----------|
| Répertoire         | [Identificateur](identifier.md) | O   | N        |
| Répertoire \_ parent | [Identificateur](identifier.md) | N   | O        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory
</dt> <dd>

La colonne Directory contient un identificateur unique pour un chemin d’accès de répertoire ou de répertoire. Cette colonne peut contenir le nom d’une propriété qui est définie sur le chemin d’accès complet d’un répertoire cible. Si cette colonne contient une propriété, le répertoire cible prend le nom spécifié dans la colonne DefaultDir et prend le répertoire parent spécifié dans la \_ colonne parente du répertoire.

Le répertoire source prend toujours le nom spécifié dans la colonne DefaultDir et prend le répertoire parent spécifié dans la \_ colonne parente du répertoire.

Si la \_ colonne parente Directory est null ou égale à la valeur de la colonne Directory, la colonne Directory représente un répertoire cible racine. Un seul répertoire racine peut être spécifié dans la table de répertoires.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Répertoire \_ parent
</dt> <dd>

Cette colonne est une référence au répertoire parent du répertoire. Un enregistrement qui a une \_ colonne parente de répertoire égale à null ou égal à la colonne de répertoire représente un répertoire racine. Le chemin d’accès complet du répertoire parent est résolu par référence dans la \_ colonne parente du répertoire est une clé externe dans la colonne Directory. Par exemple, si un dossier a un répertoire parent nommé PDIR, le répertoire parent de PDIR est indiqué dans la \_ colonne parente Directory de la ligne avec PDIR dans la colonne Directory.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

La colonne DefaultDir contient le nom du répertoire (localisable) sous le répertoire parent. Par défaut, il s’agit du nom des répertoires cible et source. Pour spécifier des noms de répertoires source et cible différents, séparez les noms de source et de source par le signe deux-points comme suit : \[ TargetName \] : \[ SourceName \] .

Si la valeur de la \_ colonne parente Directory est null ou est égale à la colonne Directory, la colonne DefaultDir spécifie le nom d’un répertoire source racine.

Dans le cas d’un répertoire source non racine, un point (.) entré dans la colonne DefaultDir pour le nom du répertoire source ou le nom du répertoire cible indique que le répertoire doit se trouver dans son répertoire parent sans un sous-répertoire.

Les noms de répertoires de cette colonne peuvent être formatés en tant que paires de noms de fichiers \| longs.

</dd> </dl>

## <a name="remarks"></a>Remarques

Chaque enregistrement de la table représente un répertoire dans les images source et de destination. La table de répertoire doit spécifier un répertoire racine unique avec une valeur de colonne de répertoire égale à la propriété [**targetDir**](targetdir.md) .

Pour une [installation administrative](administrative-installation.md), installez l’image administrative dans le répertoire racine nommé TARGETDIR et utilisez les noms des répertoires sources pour résoudre les répertoires cibles.

Remarque Le programme d’installation définit un certain nombre de [Propriétés](properties.md) standard pour les chemins d’accès de dossier système. Consultez la [référence](property-reference.md) de la propriété pour obtenir la liste des propriétés définies sur les dossiers système.

La résolution d’annuaire est effectuée pendant l' [action CostFinalize](costfinalize-action.md) et est effectuée comme suit :

### <a name="root-destination-directory"></a>Répertoire de destination racine

Il ne peut y avoir qu’un seul répertoire de destination racine. Pour spécifier le répertoire de destination racine, définissez la colonne Directory sur la propriété [**targetDir**](targetdir.md) et la colonne DefaultDir sur la propriété [**SourceDir**](sourcedir.md) . Si la propriété **targetDir** est définie, le répertoire de destination est résolu à la valeur de la propriété. Si la propriété **targetDir** n’est pas définie, la propriété [**ROOTDRIVE**](rootdrive.md) est utilisée pour résoudre le chemin d’accès.

### <a name="root-source-directory"></a>Répertoire source racine

La valeur de la colonne DefaultDir de l’entrée de répertoire racine doit être définie sur la propriété [**SourceDir**](sourcedir.md) .

### <a name="non-root-destination-directories"></a>Répertoires de destination non racine

La valeur de répertoire pour un répertoire non racine est également interprétée comme le nom d’une propriété définissant l’emplacement de la destination. Si la propriété est définie, le répertoire de destination est résolu à la valeur de la propriété. Si la propriété n’est pas définie, le répertoire de destination est résolu en un sous-répertoire sous le répertoire de destination résolu pour l' \_ entrée parente de l’annuaire. La valeur DefaultDir définit le nom du sous-répertoire.

### <a name="non-root-source-directories"></a>Répertoires sources non racines

Le répertoire source d’un répertoire non racine est résolu dans un sous-répertoire du répertoire source résolu pour l' \_ entrée parente de l’annuaire. Là encore, la valeur DefaultDir définit le nom du sous-répertoire.

### <a name="short-or-long-file-names"></a>Noms de fichier courts ou longs

Lors de la résolution des répertoires de destination, les noms de fichiers courts spécifiés dans la colonne DefaultDir sont utilisés si la propriété [**SHORTFILENAMES**](shortfilenames.md) est définie ou si le volume dans lequel se trouve le répertoire ne prend pas en charge les noms de fichiers longs. Dans le cas contraire, le nom de fichier long est utilisé.

Notez que lorsque les répertoires sont résolus au cours de l’action CostFinalize, les clés de la table Directory deviennent des [Propriétés](properties.md) définies sur des chemins d’accès aux répertoires.

[Table CreateFolder](createfolder-table.md)

Pour créer des dossiers vides pendant une installation, consultez la [table CreateFolder](createfolder-table.md).

[Utilisation de la table Directory](using-the-directory-table.md)

Pour plus d’informations sur la table de répertoires, y compris des exemples, consultez [utilisation de la table de répertoires](using-the-directory-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



