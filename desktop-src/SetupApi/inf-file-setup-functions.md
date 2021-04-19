---
description: Les fonctions suivantes de l’API d’installation sont utilisées avec les fichiers INF.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Fonctions d’installation des fichiers INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530649"
---
# <a name="inf-file-setup-functions"></a>Fonctions d’installation des fichiers INF

Les fonctions suivantes de l’API d’installation sont utilisées avec les fichiers INF.



| Fonction                                                                         | Description                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Libère des ressources et ferme le descripteur INF.                                                                                                                                                             |
| [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Copie un fichier et, si nécessaire, le décompresse.                                                                                                                                                      |
| [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Recherche la première ligne dans une section d’un fichier INF ou, si une clé est spécifiée, la première ligne correspondant à cette clé. Il met à jour le membre de **ligne** d’une structure [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) . |
| [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Retourne la ligne suivante dans une section relative au membre de **ligne** de la structure [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) spécifiée.                                                                    |
| [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Retourne la ligne suivante dans une section relative au membre de **ligne** du [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) spécifié qui correspond à une clé spécifiée.                                                 |
| [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Récupère les données d’une ligne dont les champs sont au format binaire.                                                                                                                                          |
| [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Retourne le nombre de champs dans une ligne.                                                                                                                                                                |
| [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Récupère des informations de compression de fichier à partir d’un fichier INF.                                                                                                                                               |
| [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Obtient la liste des types de fichiers INF dans un répertoire spécifié.                                                                                                                                        |
| [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Retourne des informations sur un fichier INF (par membre de **ligne** d’un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) ou d’un nom de fichier).                                                                                     |
| [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Retourne le champ entier spécifié d’une ligne dans un fichier INF.                                                                                                                                          |
| [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Met à jour le membre de **ligne** d’un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) pour la ligne à un index spécifié dans la section spécifiée.                                                                     |
| [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Retourne le nombre de lignes dans la section spécifiée.                                                                                                                                                  |
| [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Récupère le contenu d’une ligne spécifiée d’un fichier INF.                                                                                                                                            |
| [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Retourne une liste de chaînes, en commençant au champ spécifié d’une ligne dans un fichier INF.                                                                                                                   |
| [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Obtient l’ordinal et le chemin d’accès du disque source (par rapport à la racine source) où se trouve le fichier source                                                                                                       |
| [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Obtient la taille de fichier d’un fichier source individuel ou d’une section de **fichiers de copie** d’un fichier INF.                                                                                                           |
| [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Récupère le chemin d’accès, le fichier de balises ou la description d’une source.                                                                                                                                             |
| [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Retourne le champ de chaîne spécifié d’une ligne dans un fichier INF.                                                                                                                                           |
| [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Obtient le chemin d’accès cible d’une section de **fichiers de copie** dans un fichier INF.                                                                                                                                      |
| [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Installe un fichier.                                                                                                                                                                                       |
| [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Installe un fichier et retourne une variable indiquant si le fichier était en cours d’utilisation.                                                                                                                  |
| [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Met en file d’attente tous les fichiers spécifiés dans les sections **copier** les fichiers, **Supprimer les fichiers** et **Renommer les fichiers** qui sont répertoriés par une section d' **installation** .                                                       |
| [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Exécute les directives spécifiées dans une section d' **installation** du fichier INF.                                                                                                                                  |
| [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Effectue les opérations d’installation et de suppression de service telles qu’elles sont spécifiées dans la section de **service** d’un fichier INF.                                                                                            |
| [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Ouvre un fichier INF et l’ajoute à un handle INF existant.                                                                                                                                             |
| [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Ouvre un fichier INF et retourne un handle à celui-ci.                                                                                                                                                          |
| [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Ouvre le fichier INF qui contient les informations de mise en page et de fichier pour les fichiers livrés avec le système.                                                                                                        |
| [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Interroge une structure d’informations INF sur les noms de fichiers INF associés.                                                                                                                               |
| [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Interroge une structure d’informations INF pour obtenir des informations sur la version de l’un de ses fichiers INF constitutifs.                                                                                                      |
| [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Associe un nouvel identificateur de répertoire à un répertoire particulier.                                                                                                                                     |



 

 

 



