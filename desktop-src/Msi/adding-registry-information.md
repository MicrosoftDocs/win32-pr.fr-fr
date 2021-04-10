---
description: La table de Registre et les tables associées de la base de données d’installation contiennent les informations de Registre nécessaires à l’application dans le registre système.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Ajout d’informations de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951792"
---
# <a name="adding-registry-information"></a>Ajout d’informations de Registre

La [table de Registre](registry-table.md)et les tables associées de la base de données d’installation contiennent les informations de Registre nécessaires à l’application dans le registre système. Consultez le [groupe tables de Registre](registry-tables-group.md). Dans cette section, vous allez ajouter à l’exemple du bloc-notes les informations qui doivent être inscrites sur l’ordinateur de l’utilisateur.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table de Registre vide.

[Table du Registre](registry-table.md)



| Registre       | Root | Clé                                 | Nom             | Valeur    | -\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfCharSet        | \#0      | Bloc-notes     |
| ClipPrecision  | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfClipPrecision  | \#2      | Bloc-notes     |
| Escapement     | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfFaceName       | FixedSys | Bloc-notes     |
| Italique         | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfItalic         | \#0      | Bloc-notes     |
| Orientation    | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfOrientation    | \#0      | Bloc-notes     |
| Précision   | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfOutPrecision   | \#1      | Bloc-notes     |
| PageSettings   | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | fSavePageSetting | \#0      | Bloc-notes     |
| PitchAndFamily | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfPitchAndFamily | \#49     | Bloc-notes     |
| PointSize      | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | iPointSize       | \#120    | Bloc-notes     |
| Qualité        | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfQuality        | \#2      | Bloc-notes     |
| Barré      | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfStrikeOut      | \#0      | Bloc-notes     |
| Poids         | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | lfWeight         | \#400    | Bloc-notes     |
| Encapsuler           | 2    | Exemple de logiciel \\ Microsoft \\ Notepad | fWrap            | \#0      | Bloc-notes     |



 

[Continuer](specifying-shortcuts.md)

 

 



