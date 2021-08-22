---
description: le WiMakCab.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple montre comment le script est utilisé pour générer des armoires de fichier à partir d’une base de données Windows Installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Générer un fichier CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581489"
---
# <a name="generate-file-cabinet"></a>Générer un fichier CAB

le WiMakCab.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script est utilisé pour générer des armoires de fichier à partir d’une base de données Windows Installer.

Cet exemple montre :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md) et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**Méthode Commit**](database-commit.md), [**méthode OpenView**](database-openview.md) et [**propriété SummaryInformation (objet Database)**](database-summaryinformation.md) de l' [**objet Database**](database-object.md)
-   Méthode [**Fetch**](view-fetch.md), méthode [**Execute**](view-execute.md) et [**méthode modify**](view-modify.md) de l' [**objet View**](view-object.md)
-   Propriété [**StringData**](record-stringdata.md) et [**propriété IntegerData**](record-integerdata.md) de l' [**objet record**](record-object.md)
-   [**Méthode d’action**](session-doaction.md), propriété [**Property (objet session)**](session-session.md)et [**propriété mode**](session-mode.md) de l' [**objet session**](session-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiMakCab.vbs \[ chemin d’accès au nom de base de base de données \] \[ \] \[ emplacements sources facultatifs\]**

Pour générer un fichier CAB, Makecab.exe doit se trouver sur le chemin d’accès. l’utilitaire Makecab.exe est inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Notez que l’exemple ne met pas à jour la [table des médias](media-table.md) pour gérer plusieurs armoires. Pour remplacer un fichier CAB incorporé, incluez les options suivantes:/R/C/U/E.

Spécifiez le chemin d’accès à la base de données du programme d’installation. Celui-ci doit se trouver à la racine de l’arborescence source. Spécifiez le nom de base sensible à la casse pour les fichiers CAB générés. Si le type de source est compressé, tous les fichiers sont ouverts à la racine. Les options suivantes peuvent être spécifiées à n’importe quel point de la ligne de commande.



| Option              | Description                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| aucune option spécifiée |                                                                                                                                           |
| /C                  | Exécutez la compression. Si/C n’est pas spécifié, WiMakCab.vbs génère uniquement le fichier DDF.                                                        |
| /L                  | Utiliser la compression LZX au lieu de MSZIP                                                                                                      |
| /F                  | Limiter la taille du fichier cab à 1,44 Mo par rapport à la taille des disquettes au lieu du CD-ROM                                                                              |
| /U                  | Mettre à jour la base de données pour référencer le fichier CAB généré                                                                                    |
| /E                  | Incorporer le fichier cab dans le package d’installation en tant que flux                                                                               |
| /S                  | Utiliser des numéros de séquence dans la table de fichiers triée par répertoires                                                                             |
| /R                  | Revenir à une installation sans fichier CAB, supprimer le fichier cab si l’option/E est spécifiée (l’option/R supprime la propriété de bit compressé SummaryInfo 15 & 2) |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



