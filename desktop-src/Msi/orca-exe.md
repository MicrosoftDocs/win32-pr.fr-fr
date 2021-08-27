---
description: Orca.exe est un éditeur de table de base de données pour la création et la modification des packages Windows Installer et des modules de fusion.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f1b0d31936bf81e60efd8eb9799ddb30b4d5a6f78363e2ff5d3d638ae40c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082679"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe est un éditeur de table de base de données pour la création et la modification des packages Windows Installer et des modules de fusion. L’outil fournit une interface graphique pour la validation, en mettant en surbrillance les entrées particulières où se produisent des erreurs ou des avertissements de validation.

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Elle est fournie sous la forme d’un fichier de Orca.msi. après avoir installé les composants SDK Windows pour Windows Installer les développeurs, double-cliquez sur Orca.msi pour installer le fichier Orca.exe.

## <a name="syntax"></a>Syntaxe

**Orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Options de la ligne de commande

Orca.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.



| Option | Description                                                 |
|--------|-------------------------------------------------------------|
| -q     | Mode silencieux                                                  |
| -S     | <base *de données> schéma* \[ « Orca. dat »-valeur par défaut\] |
| -?     | Boîte de dialogue d’aide                                                 |



 

Orca.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse avec les modules de fusion. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret. Lorsque vous effectuez une fusion, les>-f,-m et <*sourceFile* sont tous obligatoires.



| Option     | Description                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Valider la fusion dans la base de données si aucune erreur n’est détectée.                                     |
| -!         | Validation de la fusion dans une base de données même en cas d’erreur.                       |
| -M         | <*module*> module de fusion à fusionner dans la base de données.                      |
| -f         | Fonctionnalité \[ : la \] ou les fonctionnalités feature2 pour se connecter au module de fusion.                |
| -r         | <*ID de répertoire*> entrée de répertoire pour la redirection racine du module.    |
| -X         | <*répertoire*> de l’extraction des fichiers vers une image sous le répertoire.         |
| -g         | <*langage> langage* utilisé pour ouvrir un module.                         |
| -l         | <fichier *journal*> fichier à utiliser en tant que journal, ajouter s’il existe déjà.      |
| -i         | <*répertoire*> de l’extraction des fichiers vers l’image source sous le répertoire. |
| -CAB       | <*nom* de fichier> de l’extraction de l’armoire MSM vers le fichier.                        |
| -lfn       | Utilisez des noms de fichiers longs pendant l’extraction.                                 |
| -configurer | <*filename*> configurer le module à l’aide des données d’un fichier.            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



