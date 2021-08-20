---
description: La table Directory spécifie la disposition d’une installation.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Utilisation de la table Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f550f32006df16db5811e0fbf5022253373a4b1551983ddda2db55655b4061f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141318"
---
# <a name="using-the-directory-table"></a>Utilisation de la table Directory

La [table Directory](directory-table.md) spécifie la disposition d’une installation. Lorsque les répertoires sont résolus au cours de l' [action CostFinalize](costfinalize-action.md), les clés de la table Directory deviennent des [Propriétés](properties.md) définies sur des chemins d’accès aux répertoires. Notez que le programme d’installation définit un certain nombre de [Propriétés](properties.md) standard pour les chemins d’accès de dossier système. Consultez la [référence](property-reference.md) de la propriété pour obtenir la liste des propriétés définies sur les dossiers système.

La meilleure façon de spécifier l’emplacement cible d’un répertoire consiste à créer la [table des répertoires](directory-table.md) dans votre package d’installation afin de fournir l’emplacement correct comme indiqué dans cette section. S’il est nécessaire de modifier l’emplacement du répertoire au moment de l’installation, consultez également la section : [modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md)

Voici un exemple de table de répertoires.



| Répertoire     | Répertoire \_ parent | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | Application        |
| DLLDIR        | EXEDIR            | Compartiment        |
| DesktopFolder | TARGETDIR         | Bureau    |



 

Chaque ligne de la table de répertoires indique un répertoire à la fois au niveau de la source et de la cible. Par exemple, supposons que le package d’installation se trouve au niveau de la \\ \\ source des applications \\ \\ . Étant donné que le \_ champ parent du répertoire de la première ligne a la valeur null, cet enregistrement indique les répertoires racines pour la source et la cible. Pour la source, la valeur de ce répertoire est donnée par le champ DefaultDir. La valeur par défaut de la propriété [**SourceDir**](sourcedir.md) est l’emplacement du package d’installation. Par conséquent, sauf si la propriété **SourceDir** est remplacée, le répertoire source racine est \\ \\ applications \\ source \\ .

Le champ Répertoire du premier enregistrement indique l’emplacement du répertoire cible racine. Dans ce cas, la valeur de la propriété [**targetDir**](targetdir.md) indique ce répertoire. En règle générale, la valeur de la propriété **targetDir** est définie au niveau de la ligne de commande ou par le biais d’une interface utilisateur. Dans ce cas, supposons que la propriété **targetDir** est définie sur C : \\ Program Files \\ target \\ .

Pour le deuxième enregistrement, le \_ champ parent du répertoire n’a pas la valeur null. Par conséquent, cet enregistrement indique un répertoire non racine pour la source et la cible. Dans le cas d’un répertoire source non racine, le répertoire source indiqué par l’enregistrement décrit dans le champ parent de l’annuaire \_ est le répertoire parent. Pour le deuxième enregistrement, le \_ champ parent du répertoire est TARGETDIR. Comme indiqué précédemment, le répertoire source indiqué par l’enregistrement TARGETDIR est résolu en \\ \\ \\ source applications \\ . Ainsi, le répertoire source indiqué par le deuxième enregistrement est \\ \\ \\ application source \\ applications \\ .

Un processus similaire fonctionne pour le répertoire cible. La valeur du répertoire parent pour le répertoire cible décrit dans le deuxième enregistrement est le répertoire cible résolu par le \_ champ parent du répertoire. Là encore, le \_ champ parent du répertoire contient la valeur TARGETDIR. Cela indique le premier enregistrement qui correspond à un répertoire cible de la cible C : \\ Program Files \\ \\ . Le champ Directory contient une propriété définie par l’auteur appelée EXEDIR. Si cette propriété est définie, sa valeur indique le chemin d’accès complet du répertoire. Ainsi, si cette propriété a la valeur C : \\ données \\ communes \\ , la valeur du répertoire cible indiqué par le deuxième enregistrement est c : \\ données \\ communes \\ . S’il n’est pas défini, le répertoire cible prend le nom donné par le champ DefaultDir. Dans ce cas, le répertoire cible est C : \\ Program Files \\ cible \\ app \\ .

Le même processus fonctionne pour le troisième enregistrement. Si EXEDIR et DLLDIR ne sont pas définis, le répertoire cible est C : \\ Program Files \\ target \\ app \\ bin et le répertoire source est \\ \\ applications \\ source \\ app \\ bin \\ .

Le quatrième enregistrement utilise la propriété [**DesktopFolder**](desktopfolder.md) . Si l’emplacement du Bureau de l’utilisateur est C : \\ winnt \\ Profiles \\ User \\ Desktop \\ , le répertoire cible se résout en c : \\ winnt \\ Profiles \\ User \\ Desktop \\ . Le répertoire source correspond au \\ \\ \\ Bureau source des applications \\ \\ .

Il existe deux fonctionnalités de syntaxe supplémentaires qui peuvent être utilisées dans la colonne DefaultDir de la table Directory. Dans le cas d’un répertoire source non racine, un point (.) entré dans la colonne DefaultDir indique que le répertoire doit se trouver dans son répertoire parent sans un sous-répertoire. Pour spécifier des chemins d’accès aux répertoires source et cible différents, séparez les chemins d’accès source et cible dans la colonne DefaultDir par un signe deux-points comme suit : \[ targetPath \] : \[ SourcePath \] . Ces fonctionnalités peuvent être utilisées ensemble pour ajouter des niveaux aux chemins source ou cible d’un répertoire unique. Consultez l’exemple suivant d’une table de répertoires.



| Répertoire   | Répertoire \_ parent | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | MyApp      |
| BinDir      | MyAppDir          | Compartiment        |
| Binx86Dir   | BinDir            | . : x86      |
| BinAlphaDir | BinDir            | . : Alpha    |



 

Les chemins source et cible résolvent les lignes MyAppDir, BinDir, Binx86Dir et BinAlphaDir comme suit.



| Enregistrement       | Chemins d’accès cibles            | Chemins source                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MonApp      | \[SourceDir \] MonApp             |
| BinDir:      | \[\]Emplacement du \\ magasin MonApp | \[SourceDir \] - \\ casier MonApp        |
| Binx86Dir:   | \[\]Emplacement du \\ magasin MonApp | \[SourceDir \] MyApp- \\ bin \\ x86   |
| BinAlphaDir: | \[\]Emplacement du \\ magasin MonApp | \[SourceDir \] MyApp \\ bin \\ alpha |



 

> [!Note]  
> la plateforme Alpha n’est pas prise en charge par l’Windows Installer.

 

 

 



