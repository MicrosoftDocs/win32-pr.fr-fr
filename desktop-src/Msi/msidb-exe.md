---
description: Msidb.exe utilise MsiDatabaseImport et MsiDatabaseExport pour importer et exporter des tables et des flux de base de données.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011880"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe utilise [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) et [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) pour importer et exporter des tables et des flux [de base de données](database-tables.md) .

Si le mode, le dossier, la base de données et la liste de tables sont spécifiés sur la ligne de commande, Msidb.exe n’affiche aucune interface utilisateur et fonctionne comme un utilitaire de ligne de commande silencieux adapté au script de compilation.

## <a name="syntax"></a>Syntax

**MsiDb** *{option} ***...** _{option}_* _..._ * * {table} ***...** _{table}_

## <a name="command-line-options"></a>Options de la ligne de commande

Msidb.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.



| Option | Description                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importez les fichiers d’archive de texte du dossier dans la base de données. Les noms de table pour l’importation sont des noms de fichiers de 8 caractères avec une extension « . IDT ». Les noms plus longs sont tronqués à 8 caractères s’ils sont fournis par la commande pour l’importation. Des spécifications standard de caractères génériques peuvent être utilisées.                                                                 |
| -E     | Exportez les tables sélectionnées de la base de données dans des fichiers d’archive de texte dans le dossier. Les noms de table pour l’exportation sont des noms de table. Seule la spécification générique, " \* ", peut être utilisée. Les tables peuvent être exportées à partir d’une base de données en lecture seule.                                                                                                               |
| -c     | Crée un fichier de base de données et importe des tables. Remplace un fichier de base de données existant.                                                                                                                                                                                                                                               |
| -f     | Spécifie le dossier contenant les fichiers d’archive de texte pour les tables et les flux. Si le dossier contenant les fichiers d’archive de texte n’est pas spécifié, l’utilitaire invite l’utilisateur à entrer le dossier.                                                                                                                                       |
| -d     | Chemin d’accès complet au fichier de base de données.                                                                                                                                                                                                                                                                                          |
| -M     | Chemin d’accès complet à la base de données dans laquelle la fusion doit être fusionnée. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10. Si la base de données n’est pas spécifiée sur la ligne de commande, l’utilitaire invite l’utilisateur à entrer la base de données.                                       |
| -T     | Chemin d’accès complet à la transformation à appliquer. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10.                                                                                                                                                     |
| -j     | Nom du stockage à supprimer de la base de données. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10.                                                                                                                                                             |
| -k     | Nom du flux à supprimer de la base de données. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10.                                                                                                                                                                 |
| -X     | Nom du flux à enregistrer dans un fichier sur disque dans le répertoire actif. Cette option est disponible uniquement en mode de ligne de commande silencieux. Les flux de données binaires sont stockés sous forme de fichiers séparés avec l’extension « . IBD ». Le nom de fichier binaire utilisé correspond aux données de clé primaire de la ligne contenant le flux.                                                  |
| -w     | Nom du stockage à enregistrer dans un fichier sur disque dans le répertoire actif. Cette option est disponible uniquement en mode de ligne de commande silencieux.                                                                                                                                                                                                         |
| -a     | Nom du fichier à ajouter à la base de données sous forme de flux. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10. Les flux de données binaires sont stockés sous forme de fichiers séparés avec l’extension « . IBD ». Le nom de fichier binaire utilisé correspond aux données de clé primaire de la ligne contenant le flux. |
| -r     | Nom du stockage à ajouter à la base de données en tant que sous-stockage. Cette option est disponible uniquement en mode de ligne de commande silencieux. Plusieurs instances de cette option peuvent avoir une valeur maximale de 10.                                                                                                                                                     |
| -S     | Tronque les noms de table à 8 caractères lors de l’exportation vers un. IDT. Le nom de la table est tronqué à 8 caractères et l’extension « . IDT » est ajoutée.                                                                                                                                                                                           |
| -?     | Affiche la boîte de dialogue d’aide de la ligne de commande                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Lorsque vous utilisez des noms de fichiers longs avec des espaces, utilisez des guillemets autour. Par exemple, pour une base de données qui se trouve dans le dossier « Mes documents », spécifiez-la sous la forme « c : \\ Mes documents ».

 

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



